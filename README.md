About
=====

Shared content, templates and help files for JJA

Main site content goes in brands/default

Each brand must have a configuration block in brands.json and its own directory in the brands folder. e.g. sparerib is in brands/sparerib

Templates
=========

All templates are html files, there are no restrictions on the HTML that can go inside.

If a custom brand doesn't have a specific version of a template (or image) the default will be used instead.

For example if you link to /britishlibrary/sparerib/sitemap and the routes.js file has a mapping of "sitemap" to "sitemap/sitemap.html" the template
system will first look for /brands/sparerib/sitemap/sitemap.html and if that doesn't exist it will look for /brands/default/sitemap/sitemap.html

Linking
=======

When linking to the site always use absolute URL paths without the domain name : e.g. '/about' not 'http://journalarchives.jisc.ac.uk/about'.

URL mappings for static content must be configured in routes.js (see below)

Images
======

Images should also be linked using absolute URL paths, e.g. /images/support/logos/mimas.gif.

For brand specific images the format is /images/BRAND_ID/path/to/image. e.g. /images/sparerib/banner.jpg
Brand image URLs only use the short brand id NOT the URL fragment defined in brands.json (/britishlibrary/sparerib)

As with templates if a brand specific image is not found the default will be loaded instead if it exists.

Configuration
=============

routes.js
---------

This is where you map site URLs to files.

For example the 'about' page for JA is available via the URL journalarchives.jisc.ac.uk/about and the html template is in brands/default/about/about.html
 
The route configuration for the about page is :
 
 "about" : "about/about.html"
 
The URL fragment is in the left and the file is on the right. URL fragments are relative to the root of the site (journalarchives.jisc.ac.uk) and files are 
relative to the current brand, e.g. /brands/default/

brands.json
-----------

Configuration for custom brands.

id    : Unique identifier, used as directory name for that brands content.

title : Name of the brand to be displayed on site.

url   : base path for the brand URLs, e.g. "/britishlibrary/sparerib"

filter : search filter field

images :
  banner/path : banner image to appear in search results tabs
  footer/logo : additional footer logo image to go alongside the JISC logo.