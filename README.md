# Destiny.gg
Source code for the website http://www.destiny.gg/
Work in progress...

## Requirements
[composer](http://getcomposer.org/download/) is required to pull dependencies.


## Installation
Add your custom configuration file to /config/config.local.php, override what you need.

Composer setup
	>composer upgrade
	
Pack files build
	>php -f "scripts/pack.php"

Install the database structure
	destiny.gg.sql


## The cron
All api requests and heavy tasks are done on a single cron task (currently running every 60 seconds on the live server)
This is controlled by "Tasks".

If you are running the website locally, you can call this file manually, or setup a cron.

/cron/index.php

The table "[prefix_]scheduled_tasks" will show when specific tasks have been run.

If you don't run this, you will get no data in the site.