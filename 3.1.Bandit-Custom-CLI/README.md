## Bandit-Custom-CLI
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/3.0.Bandit-Custom-CLI`
* Step 3: Activate virtualenv 

	`source venv/bin/activate`
* Step 4: Run bandit 
	
	`bandit -f json -o bandit-result.json -x /home/vagrant/sources/Vulnerable-Flask-App/app/venv -r /home/vagrant/sources/Vulnerable-Flask-App/`
* Step 5: View report
	
	`firefox file://$PWD/bandit-result.json`
* Step 6: Deactivate virtualenv
	
	`deactivate`
