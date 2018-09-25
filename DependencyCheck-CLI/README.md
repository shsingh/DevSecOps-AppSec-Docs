## DependencyCheck-CLI
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/DependencyCheck-CLI/dependency-check/bin`
* Step 3: Run Dependency Check 
	
	`sh dependency-check.sh -n -f HTML -f XML --project "Test Scan" --scan "/home/vagrant/sources/HacmeBooks"`
* Step 4: View report
	
	`firefox dependency-check-report.html`

