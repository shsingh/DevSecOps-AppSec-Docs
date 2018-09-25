## RetireJS-CLI
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/RetireJS-CLI`
* Step 3: Run RetireJS Scan 
	
	`retire --path /home/vagrant/sources/Cut-The-Funds-NodeJS --outputformat json --outputpath $PWD/retirejs-report.json`
* Step 4: View report
	
	`firefox file://$PWD/retirejs-report.json`

