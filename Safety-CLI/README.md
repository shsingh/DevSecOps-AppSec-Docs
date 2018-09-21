## Safety-CLI
* Step 1: Open terminal

* Step 2: Change directory

	 `cd /home/vagrant/sources/Vulnerable-Flask-App/app`
	 
* Step 3: Activate virtualenv
	
	`source venv/bin/activate`	
	
* Step 4: Run `safety` python package scanner 
	
	`safety check --json`
    
* Step 5: Vulnerable packages will be listed on screen

* Step 6: Deactivate virtualenv
	
	`deactivate`


	

