# Lua Scripts and Modules for Garry's mod


## Github Repository Checker 



```	
Idea and creation by General Wrex & Bubbus with credits to Nebual 

***Include this into a file thats loaded before others, DONT PUT IN AUTORUN!!!***

GitRC.CheckVersion(RepoOwner, RepoName, Callback):
**http://github.com/RepoOwner/RepoName**
	
Args:
	RepoOwner:  
		The owner of the repository
	RepoName:
		The name of the repository
	Callback:
		Returns the parsed data from the repository:
	


 * Useful variables: *
			
	data.uptodate: (bool)
		Returns true if the players addon is up to date with the repositories.
	data.name: (string)
		Returns the repository owner
	data.commits (table)
		Returns up to 10 commits ( default ) with the first entry being the latest
```	
	
Example:
```	
		GitRC.CheckVersion("nrlulz", "ACF", function(data)
			print(data.name.." is "..data.uptodate and "Up To Date" or "Out Of Date")
		end)
```	

