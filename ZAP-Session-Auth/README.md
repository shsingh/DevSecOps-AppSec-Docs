## ZAP "Canned Sessions" Authentication

Make sure you have `vul_flask` running, else start with `start-vul-flask`

* Step 1: Open "home" on Desktop
* Step 2: Navigate to ﻿`/home/vagrant/Labs/ZAP-Basics/ZAP-Mini-Workshop/orig_session/`
* Step 3: Copy all files in directory: `Select All`, `Copy`
* Step 4: Paste in  `/home/vagrant/Labs/ZAP-Basics/ZAP-Mini-Workshop/temp_session/`
* Step 5: Open Terminal and enter `start-zap-gui` and wait for OWASP ZAP to Start
* Step 6: In the top left `File` menu, click on `Open Session`
* In the file select prompt, navigate to `/home/vagrant/Labs/ZAP-Basics/ZAP-Mini-Workshop/temp_session/`
* Select `api.session` in the temp_session directory. It should load a session with history of URL requests
* Right click on `localhost:5050` from Sites and select `Attack > Active Scan`
* Select the Light Policy and wait for Scan to be complete
* Close ZAP