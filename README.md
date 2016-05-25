# Lua Scripts and Modules for Garry's mod


##Github Repository Checker 

    Github Version Checker v1 
	
	based on Github Repository Checker 
	
	  Created by General Wrex & Bubbus
		
	  Credits: Nebual
	

	***Include this into a file thats loaded before others, DONT PUT IN AUTORUN!!!***


	GitC.CheckVersion(RepoOwner, RepoName, Callback):
	
	**http://github.com/RepoOwner/RepoName**
	
	Args:
		RepoOwner:  
			The owner of the repository
			
		RepoName:
			The name of the repository
		
		Callback:
			Returns the parsed data from the repository:
	
			Useful variables:
			
				data.uptodate: (bool)
					Returns true if the players addon is up to date with the repositories.
				data.name: (string)
					Returns the repository owner
				data.commits (table)
					Returns up to 100 commits with the first entry being the latest

	
	Example:
	
		GitRC.CheckVersion("nrlulz", "ACF", function(data)
			print(data.name.." is "..data.uptodate and "Up To Date" or "Out Of Date")
		end)
	

