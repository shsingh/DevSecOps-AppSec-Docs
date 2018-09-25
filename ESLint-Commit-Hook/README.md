## ESLint-Commit-Hook
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/ESLint-Commit-Hook/Cut-The-Funds-NodeJS`
* Step 3: Create a file with the following content and save it
	
	```
	var exec = require('child_process').exec;
    exec('node -v', function(error, stdout, stderr) {
       console.log('stdout: ' + stdout);
    });
    ```
    
* Step 4: Add the file to git repo
	
	`git add -A`
* Step 5: Now commit the file to git repo
	
	`git commit -m "Commited insecure javascript file"`
* Step 6: Now the ESLint will trigger a scan and reports few warnings and errors		
	

