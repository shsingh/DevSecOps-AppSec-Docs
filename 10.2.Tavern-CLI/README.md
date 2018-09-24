## Tavern CLI
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/10.2.Tavern-CLI`
* Step 3: Activate virtualenv
	
	`source venv/bin/activate`	
	
* Step 4:	Start the application and wait for few minutes

	` docker-compose up -d`

* Step 5: Wait for few seconds (approx 40 sec) for the application to boot up	
	
* Step 6: Run Tavern shell script 
	
	`sh run.sh`
    
* Step 7: View test results log
	
	`cat result.log`
	
* Step 8: Stop application

	`docker-compose down`
	
* Step 9: Deactivate virtualenv

	`deactivate`
	

