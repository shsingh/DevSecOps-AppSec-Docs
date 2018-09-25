## NodeJsScan-CLI
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/NodeJsScan-CLI`
* Step 3: Activate virtualenv 

	`source venv/bin/activate`
* Step 4: Run NodeJsScan 
	
	`nodejsscan -d /home/vagrant/sources/Cut-The-Funds-NodeJS -o nodejscan-report`
* Step 5: View report
	
	`firefox file://$PWD/nodejscan-report.json`
* Step 6: Deactivate virtualenv
	
	`deactivate`	
