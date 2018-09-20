## RoboZAP
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/12.1.RoboZAP`
	 
* Step 3: Activate virtualenv
	
	`source venv/bin/activate`	
	
* Step 4: Start vulnerable flask app

	`start-vul-flask`
	
* Step 5:	Run robot scan

	`robot zap_test.robot`
	
* Step 6: ZAP opens on a new window
	
	![Image](./img/zap_open.png)
    
* Step 7: ZAP status of the scan will look like this
	
	![Image](./img/zap-status.png)
	
* Step 8: Once the scan is done the Command line will have the following status screen

	![Image](./img/robozap-status.png)
	
* Step 9: Deactivate virtualenv

	`deactivate`
	
* Step 10: Stop flask app
	`clean-doc`
	

