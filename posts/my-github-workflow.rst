.. title: My github workflow
.. slug: my-github-workflow
.. date: 2018-06-04 01:48:13 UTC+07:00
.. tags: github
.. category: software
.. link: 
.. description: 
.. type: text

Select branch e.g. master branch. the current branch is called HEAD::

	git checkout master
	
check HEAD::

	cat .git/HEAD
	
modify the code then commit::

	git commit -m "leave some note here"
	
we might want to undo commit::

	git reset --hard HEAD~1
	
or undo to specified commit::

	git reset --hard commit_sha
	
check your local branch with the remote::

	git status
	
push the local commits to remote branch e.g. remote name "origin", branch name "master"::

	git push origin master
	
more common command check::

	git help everyday
	
	

