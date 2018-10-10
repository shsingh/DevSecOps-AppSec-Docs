## Custom Regression Script - Robot Framework

* Step 1: `cd ﻿/home/vagrant/Labs/NodeRoboPipeline`
* Step 2: Copy the Test Cases from the `RegressionScript.txt` and paste it after the ZAP Active Scan test case in pipeline.robot (after line 61)

```
﻿ZAP Active Scan
    ${scan_id}=  zap start ascan  ${CONTEXT_ID}  ${ZAP_TARGET}  ${SCANPOLICY}
    set suite variable  ${SCAN_ID}  ${scan_id}
    zap scan status  ${scan_id}
    zap write to json file  ${ZAP_TARGET}

<<<NEW PASTED CONTENT>>
Auth Custom Exploit
    [Tags]  custom_exploit
    Authenticate to web service as a regular user

Create Expense for Custom Exploit
    [Tags]  custom_exploit
    [Setup]  Set Headers  { "Authorization": "${TOKEN}" }
    Create a Regular Expense
    Update Expense with Approved Tag
```

* Step 3: After all the test cases, paste the Keywords section from `RegressionScript.txt` (After line 67)

```
*** Keywords ***
Authenticate to web service as a regular user
    &{res}=  POST  /users/login  {"email": "maya.williams@widget.co", "password": "superman123"}
    Integer  response status  200
    Boolean  response body auth  true
    set suite variable  ${TOKEN}  ${res.body["token"]}
    log  ${TOKEN}

Create a Regular Expense
    &{res}=  POST  /expenses/create_expense  {"name": "Dinner at TGIF", "projectId": "5ace0e85b10d64111c00adb2", "merchant": "TGIF", "reason": "Food Expenses at Conference", "amount": 80}
    Integer  response status  201
    set suite variable  ${EXPENSE_ID}  ${res.body["expense"]}
    log  ${EXPENSE_ID}

Update Expense with Approved Tag
    &{res}=  POST  /expenses/update_expense/${EXPENSE_ID}  {"isApproved": true}
    Integer  response status  200
    ${vul_name}=  convert to string  Insecure Direct Object Reference - Mass Assignment
    ${tool}=  convert to string  Custom Exploit Script
    ${cwe}=  convert to integer  285
    ${description}=  convert to string  The update expense function is vulnerable to a Mass-Assignment style Insecure Direct Object Reference, where the attacker can guess the name of the named parameters and bypass authorization"
    ${severity}=  convert to integer  3
    &{vul_dict}=  Create Dictionary  name=${vul_name}  tool=${tool}  cwe=${cwe}  description=${description}  severity=${severity}  target_name=${TARGET_NAME}
    run keyword if  ${res.body["isApproved"]}==True  create vulnerability  ${vul_dict}
```

* Step 4: Follow the Instructions for `NodeRobotPipeline` from now on