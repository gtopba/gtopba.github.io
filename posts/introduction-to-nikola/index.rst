.. title: Introduction to Nikola.
.. slug: introduction-to-nikola
.. date: 2017-07-06 22:13:28 UTC+07:00
.. tags: nikola
.. category: 
.. link: 
.. description: 
.. type: text


About Nikola
================

Nikola is a static site and blog generator written in Python. Nikola-based sites don't run any code on the server, there is no way to process user input in forms. You can have animations, slides or whatever fancy CSS3/HTML5 thingie you like. It only means all that HTML is generated already before being uploaded.

On the other hand, most "modern" websites are dynamic in the sense that the contents of the site live in a database, and are converted into HTML only when a user wants to see the page. However, on dynamic sites, every time a reader wants a page, a whole lot of database queries are made. Then a whole pile of code chews that data, and HTML is produced, which is sent to the user. All that requires CPU and memory.

On a static site, the highly optimized HTTP server reads the file from disk (or, if it's a popular file, from disk cache), and sends it to the user. You could probably serve a bazillion (technical term) page views from a phone using static sites.

Using Nikola on Windows can be a little trickier. Most tutorial out there are mostly based on Linux and MacOS. As a Windows user, I sometime failed to follow those tutorials. However, you will just have to get through it once then you will be fine. Let's get started.

Preparing a development environment
------------------------------------
Nikola runs on Python. So we need to install Python and necessary modules. All the modules will be installed inside an isolated Python virtual environment with it own libraries and site-packages. Virtual environment allows you to work on more than one project separately. 

Note that I am using windows. Some command-line syntax may differ from other operating systems. There are several ways to install modules on Python. If you are interested in this topic, I would recommend you to check this out https://www.youtube.com/user/sentdex

1. Download and install the latest version of Python at https://www.python.org/downloads/release/python-361/
2. Install virtualenv module by running this command in you terminal. In this case, the Windows command line (Start>cmd)::

	py -m pip install virtualenv

3. Install virtualenvwrapper-win. Using the virtualenv through this wrapper is much easier::

	py -m pip install virtualenvwrapper-win
	
4. Create a virtual environment with any name such as "nikola"::

	mkvirtualenv nikola
	
5. Install Nikola package::

	pip install --upgrade "Nikola[extras]"
	
Now you are ready to generate the first website. The next post will teach you how to genrate a static website. I would reccomend you to check out your new environment folder at C:/Users/[username]/Envs. Also learn more about the virtualenvwrapper command on their mainpage.

.. Note:: UPDATE 2018-05-15 : I have found a simpler way to create virtual environment and manage packages `here <link://slug/using-python-virtual-environment-with-anaconda>`_