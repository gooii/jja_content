Shared content, templates and help files for JJA

Main site content goes in brands/default

Each brand must have a configuration block in brands.js and its own directory in the brands folder. e.g. sparerib is in brands/sparerib

Images are placed in the brands/BRAND/images folder

If a custom brand doesn't have a specific version of a file the default will be used instead. This applies to both html templates and images.

Linking
=======

Images
======


Configuration
=============

brands.js
---------



routes.js
---------

This is where you map site URLs to files.

For example the 'about' page for JA is available via the URL journalarchives.jisc.ac.uk/about and the html template is in brands/default/about/about.html
 
 The route configuration for the about page is :
 
 "about" : "about/about.html"
 
 The URL fragment is in the left and the file is on the right. URL fragments are relative to the root of the site (journalarchives.jisc.ac.uk) and files are 
 relative to the current brand, e.g. /brands/default/