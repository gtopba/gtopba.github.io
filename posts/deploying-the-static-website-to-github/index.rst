.. title: Deploying the static website to GitHub.
.. slug: deploying-the-static-website-to-github
.. date: 2017-07-06 22:24:34 UTC+07:00
.. tags: nikola, github, git
.. category: building_website
.. link: 
.. description: 
.. type: text


Assuming you already created a github.io repository following the instruction from this link https://pages.github.com/ and already install the 'Git<https://git-scm.com/downloads>'_ software according to your operating system. Given the original 'github_deploy<https://getnikola.com/handbook.html#deploying-to-github>'_ tutorial, I will explain more where you might get confused.

Initialize a git repository in your Nikola source directory by running::

	git init.
	git remote add origin git@github.com:user/repository.git
	
+ user : your Github username, for example, "deadbeef"
+ repository : your github.io repository, for example, deadbeef.github.io.git
	
so the command should be::
	
	git remote add origin git@github.com:deadbeef/deadbeef.github.io.git
		
Then, setup conf.py::

	GITHUB_SOURCE_BRANCH = 'src'
	GITHUB_DEPLOY_BRANCH = 'master'
	GITHUB_REMOTE_NAME = 'origin'
	GITHUB_COMMIT_SOURCE = True
	
+ 'src' means your Nikola source branch's name is src
+ 'master' means your compiled static website branch's name is master

Create a .gitignore file containing::

	cache
	.doit.db
	__pycache__
	output
	
Finally, deploying::

	nikola github_deploy
	
first time it will ask you to log in to your github account. Then, you should be able to access you website https://deadbeef.github.io

