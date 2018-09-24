## Bandit-CLI
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/2.1.Bandit-CLI`
* Step 3: Activate virtualenv 

	`source venv/bin/activate`
* Step 4: Run bandit 
	
	`bandit -r -f html -o bandit-result.html /home/vagrant/sources/CTF2`
* Step 5: View report
	
	`firefox file://$PWD/bandit-result.html`
* Step 6: Deactivate virtualenv
	
	`deactivate`
