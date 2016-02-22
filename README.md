This adds search shortcuts to Chrome, Firefox and Internet Explorer on Windows PCs.

These are both useful and a pain to edit manually, hence this project.

See e.g. http://kb.mozillazine.org/Using_keyword_searches for details or http://lifehacker.com/5476033/how-to-set-keyword-bookmarks-in-google-chrome for details. 

Use
===

Run ```addSearchShortcuts.bat``` to add the default file, which is ```searches.xml```. 

Alternatively drag XML files on to ```addSearchShortcuts.bat``` to add other files, such as dictionaries.xml, which adds a load of dictionary
search shortcuts.

Chrome and Firefox will be killed when this runs! 

You can also use a ```/s``` switch to run it in silent mode, without keyboard prompts, although admin rights will be required for Internet 
Explorer registry entries

You could create additional XML files for further shortcuts, or edit these.

Workings
=========

* ```msmsl.exe``` is used to convert ```searches.xml``` into SQLite (for Chrome and Firefox) and registry (for internet explorer) files
containing details of the search shortcuts, using the XSL files in the ```xsl``` directory.
* These are then added to the SQLite databases and registry respectively.
