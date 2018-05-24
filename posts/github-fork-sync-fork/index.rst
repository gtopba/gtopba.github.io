.. title: Github Fork, Sync Fork
.. slug: github-fork-sync-fork
.. date: 2018-05-24 15:20:52 UTC+07:00
.. tags: git, github
.. category: software
.. link: 
.. description: 
.. type: text

Fork
=====
In the top-right corner of the page, click Fork. That's it! Now, you have a fork of the original repository. You can now modified your fork without effecting the original repo. New commits from the main repo won't effect your fork. You need to manually sync your fork with the original repo.

Sync Fork
=========
Create a local clone of your fork::

	git clone https://github.com/YOUR-USERNAME/YOUR-FORK.git
	
sync your fork with the original repository::

	git remote -v
	git remote add upstream https://github.com/ORIGINAL-OWNER/ORIGINAL-REPO.git
	git remote -v
	git fetch upstream
	
Check out your fork's local master branch.::

	git checkout master 
	
Merge the changes from upstream/master into your local master branch. This brings your fork's master branch into sync with the upstream repository, without losing your local changes.::
	
	git merge upstream/master
	
push commits made on your local branch to a remote repository.::

	git push  <REMOTENAME> <BRANCHNAME> 
	
As an example, you usually run git push origin master to push your local changes to your online repository.

|

References
----------

| `Fork a repo <https://help.github.com/articles/fork-a-repo/>`_
| `Authenticating with GitHub from Git <https://help.github.com/articles/set-up-git/#next-steps-authenticating-with-github-from-git>`_
| `Syncing a fork <https://help.github.com/articles/syncing-a-fork/>`_
| `Pushing to a remote <https://help.github.com/articles/pushing-to-a-remote/>`_