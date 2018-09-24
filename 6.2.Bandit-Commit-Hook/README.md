## Bandit-Commit-Hook
* Step 1: Open terminal
* Step 2: Change directory

	 `cd /home/vagrant/Labs/6.2.Bandit-Commit-Hook`
* Step 3: Activate virtualenv
	
	`source venv/bin/activate`	
	
* Step 4:	Change Directory to Vulnerable Flask App

	` cd Vulnerable-Flask-App/`
	
* Step 5: Create a python file with the following content and save it 
	
	```python
	import yaml
	with open("example.yaml", 'r') as stream:
		try:
			print(yaml.load(stream))
		except yaml.YAMLError as exc:
			print(exc)
    ```
    
* Step 6: Add the file to git repo
	
	`git add -A`
* Step 7: Now commit the file to git repo
	
	`git commit -m "Commited insecure python file"`
	
* Step 8: Now the Bandit will trigger a scan and reports few errors
* Step 9: Deactivate virtualenv
	
	`deactivate`		
	

