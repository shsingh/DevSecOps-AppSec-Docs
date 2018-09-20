## Tavern CLI
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/10.2.Tavern-CLI`
* Step 3: Activate virtualenv
	
	`source venv/bin/activate`	
	
* Step 4:	Start the application and wait for few minutes

	` docker-compose up -d && sleep 10`
	
* Step 5: Run Tavern shell script 
	
	`sh run.sh`
    
* Step 6: View test results log
	
	`cat result.log`
	
* Step 7: Stop application

	`docker-compose down`
	
* Step 8: Deactivate virtualenv

	`deactivate`
	

