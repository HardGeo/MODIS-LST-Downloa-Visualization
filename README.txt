***********************MODIS Download and Processing QGIS Plugin****************************************************************************
author: Jonas Apelt
mail: jonas.apelt@gmx.de
Martin-Luther-Universität Halle
============================================================================================================================================
                                    How to install
============================================================================================================================================ 

* Copy the entire folder called "modis" containing the new plugin to the QGIS plugin
 directory

 e.g. C:/Users/USER/AppData/Roaming/QGIS/QGIS3/profiles/default/python/plugins
* Compile the resources file creating a new text file with following content: 

   call "C:\OSGeo4W64\bin\o4w_env.bat"
   call "C:\OSGeo4W64\bin\qt5_env.bat"
   call "C:\OSGeo4W64\bin\py3_env.bat"

   @echo on
   pyrcc5 -o resources.py resources.qrc

*  replace the C:\OSGeo4W64\bin\ with your path
*  save the text file to the plugin folder as "compile.bat" and replace the old file
*  run the compile.bat file in the plugin folder


* Test the plugin by enabling it in the QGIS plugin manager

  
* Customize it by editing the implementation file: ``MODIS.py``

  
* Create your own custom icon, replacing the default icon.png

  
* Modify your user interface by opening MODIS_dialog_base.ui in Qt Designer

  
* You can use the Makefile to compile your Ui and resource files when
 you make changes. 
  This requires GNU make (gmake)

For more information, see the PyQGIS Developer Cookbook at:

  http://www.qgis.org/pyqgis-cookbook/index.html

(C) 2011-2018 GeoApt LLC - geoapt.com


=============================================================================================================================================
                             What's important
=============================================================================================================================================
If an error occurs about a missing file called 'proj.db' add a new PATH variable in windows called PROJ_LIB and add the path were 'proj.db' is saved.
Reboot your system and it should work.

If you enter tiles manually, please do it as following: h18v03, h17v03
Seperate by comma. h=0-35 v=0-17; never use white spaces in your path, if your username contains white space, 
use a different folder.

Before starting the Plugin it's recommended to activate a standard map (like OSM) of your choice to enable 
automatic tile selection of your current scene.

Please note that MODIS Terra was launched in 1999 and Aqua in 2002, so no data will be available before and error occurs.

For clarity use Suffix endings to determine files from differrent executions

GOOD LUCK! Please report errors if Errors occure!




