.. title: An empty website and its folder structure.
.. slug: generating-an-empty-website
.. date: 2017-07-06 22:16:58 UTC+07:00
.. tags: nikola
.. category: 
.. link: 
.. description: 
.. type: text

.. sidebar:: Tip: Demo site

   You can generate a website containing demo contents in it by using --demo option:: 
   
		nikola init --demo my_first_site
   
Now let's generate an empty site with any name such as "my_first_site". Navigate your terminal to the directory that you want to put your project folder on. Then run this command and follow its instructions::

	nikola init my_first_site

Then create your first post and it will ask you to input post title. Your post file .rst will be created in "posts" folder. We will edit the post later::

	nikola new_post
	
Build your website::

	nikola build
	
Let's see your empty website on the browser. The -b option will open your default web browser automatically::

	nikola serve -b

Press Ctrl+C to stop your web server.

The project's folder structure.
--------------------------------

After the initialization, you will get folder like this.

.. image:: /pic/nikola-tut/folder_struc.JPG
   :height: 235px
   :width: 267 px
   :scale: 100 %
   :alt: Folder Structure
   :align: left

============  ============ 
 **Name**     **Description** 
------------  ------------ 
files		  Everything in here will be copied to your output folder. 
galleries     Put your images folder here to generate gallery page.
listings	  Put your code here to show it. (`Learn more <link://slug/listings-demo>`__ )
output		  Your generated website. 
pages		  All your pages are kept here. 
post   		  All your posts are kept here.
conf.py       settings for Nikola.
============  ============

|
|

Next post, we will customize our site.

