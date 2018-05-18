.. title: Using Python virtual environment with Anaconda
.. slug: using-python-virtual-environment-with-anaconda
.. date: 2018-05-15 11:41:20 UTC+07:00
.. tags: 
.. category: 
.. link: 
.. description: 
.. type: text

Anaconda is an easier way for beginner to lean Python. We can create Python virtual environments for both 2.7 and 3.6 without messing around with the system PATH. In fact, you don't even need Administrator privilege. Moreover, you can manage Python modules through the GUI package manager. There are other useful tools such as Spyder IDE and Jupyter Notebook which we will talk about in the future. In `Introduction to Nikola <link://slug/introduction-to-nikola>`_ , I created an environment using virtualenv and virtualenvwrapper-win packages which is fine, but there is a simpler method. Let's get started.

Download and install 
	Download latest version of `Anaconda <https://www.anaconda.com/download/>`_ . I installed the Python 3.6 version. However, you still can create Python 2.7 environment.

	.. figure:: /pic/nikola-tut/anaconda/nikola-pic.JPG
	   :alt: Anaconda Navigator.
	   
	   Anaconda Navigator.
	   
Create new environment	
	From the left, select Environments tab and create new environment with python 3.6 as show in figure below.
	
	.. figure:: /pic/nikola-tut/anaconda/nikola-pic-1.JPG
	   :alt: Creating new environment.
	   
	   Creating new Python 3.6 environment.
   
Install desired package in the environment
	Start the environment terminal
	
	.. figure:: /pic/nikola-tut/anaconda/nikola-pic-2.JPG
	   :alt: Terminal with Python virtual environment
	   
	   Terminal with Python virtual environment.

	Install Nikola package::
	
		pip install --upgrade "Nikola[extras]"
	
