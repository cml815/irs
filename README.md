** Purpose of project: ** Speed the access of foundation IRS data uploaded by bulk.resource.org. 


README from Public Resource Org on its reports on tax exempt organizations: https://bulk.resource.org/irs.gov/eo/readme.html

This project only extracts data organizations characterized as Private Foundations (Type PF). 

** Project Tasks (In progress): ** 


----------------
README from original source code available on Github [here](https://github.com/lukerosiak/irs)

Use PostGreSQL full-text search and Django on an index compiled from a zip file to search all IRS nonprofits' financial docs (990s) by nonprofit name, as uploaded by bulk.resource.org.

Application adapted from: 

By Luke Rosiak, a reporter at the Washington Times (lukerosiak.info)

A working instance of this tool is available http://lukerosiak.info/irs/

Released under the GNU license

To use this django app:

createdb [database name] (if you aren't already using postgres with existing django apps)

psql [database name] < create.sql (instead of manage.py syncdb)

python manage.py nonprofit_import (this will take a long time. Run this monthly) 

Fix namespacing by removing 'quarterback.' from the import statements in views.py and management/commands/nonprofit_import.py. Remove my google analytics code from /templates/nonprofits.html

Go to /irs/ on your server
