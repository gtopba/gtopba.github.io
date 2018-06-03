.. title: Adding an existing project to GitHub
.. slug: adding-an-existing-project-to-github
.. date: 2018-06-04 01:48:57 UTC+07:00
.. tags: github
.. category: software
.. link: 
.. description: 
.. type: text

1. Create a new repository on GitHub. To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub. 

2. Initialize the local directory as a Git repository.::

	git init
	
3. Add the files in your new local repository. This stages them for the first commit. '.' means all files::

	git add .
	
4. Commit the files that you've staged in your local repository.::

	git commit -m "First commit"
	
5.  add the URL for the remote repository where your local repository will be pushed.::

	git remote add origin remote repository URL
	git remote -v
	
6. Push the changes in your local repository to GitHub.::

	git push origin master
	
References
----------
`Adding an existing project to GitHub using the command line <https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/>`_

