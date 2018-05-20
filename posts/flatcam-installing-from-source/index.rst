.. title: Flatcam installing from source
.. slug: flatcam-installing-from-source
.. date: 2018-05-18 18:50:07 UTC+07:00
.. tags: flatcam, pcb
.. category: 
.. link: 
.. description: 
.. type: text

Create new Python 2.7 environment and install dependencies.
	Follow this tutorial `Using Python virtual environment with Anaconda <link://slug/using-python-virtual-environment-with-anaconda>`_. Then open up your new environment terminal. Make sure it is python 2.7 by::
	
		python -V
		
	Install packages::
	
		pip install matplotlib
		pip install pypiwin32
		pip install pywin32
		pip install svg.path
		pip install scipy
		
	note : Numpy already existed in the Anaconda environment. Use this command to check available package::
	
		pip freeze
	
	These packages are for Windows user. The .whl file is a pre-compiled package with its dependencies included. Simply download the following Python 2.7 64-bit packages and navigate your terminal to the containing folder.
	
	+ `PyQt4 <http://www.riverbankcomputing.co.uk/software/pyqt/>`_
	+ `Shapely <https://github.com/Toblerity/Shapely>`_
	+ `RTree <https://github.com/Toblerity/rtree>`_
	+ `Simplejson <https://github.com/simplejson/simplejson>`_
	
	Run this command to install the packages::
	
		pip install <package's name>
		
	From `original requirements <http://www.flatcam.org/manual/installation.html#required>`_ , it suggests Python 2.7 32-bit. I have not found any problem using Python 2.7 64-bit version.

Clone Flatcam repository and run it
	navigate your terminal to where you want to put the clone and run this::
	
		git clone https://bitbucket.org/jpcgt/flatcam
		cd flatcam
		python flatcam

	Enjoy the Flatcam ! This is not stable release and may contain bugs, use it at your own risk.