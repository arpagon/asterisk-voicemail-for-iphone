### Asterisk Voicemail for iPhone ###
Copyright 2008 Chris Carey (http://chriscarey.com).
This program is distributed under the terms of the GNU General Public License

## Introduction ##

**This software is not a native iPhone app.** It is a web application which is installed on your Asterisk server. You access the software by using your iPhone web browser and accessing a URL on your Asterisk server.

## PHP Version ##

PHP4 or PHP5 are both supported.

## Apache Setup ##

Change apache default user and group to asterisk. For the software to be able to delete and move messages, it must have read/write access to all the asterisk files. This accomplishes that. (Maybe we can get away with just changing the group on a later version?)

  * User asterisk
  * Group asterisk

For me, /var/lib/php5 needed to be chowned to asterisk for session\_start() to work. There may be other folders that need to be chowned to asterisk due to the web server running as asterisk. Check your apache error log for messages.

## Dependency Install ##

  * Install Lame on your web server (for mp3 creation). Debian based systems: **apt-get install lame**
  * Install php-curl IF you have 'check for updates' enabled. Debian based systems: **apt-get install php5-curl**

## Install files in the application folder ##

After you unzip the asterisk-voicemail-for-iphone.zip file, go ahead and rename that folder to **iphone** and move it to /var/www/ or wherever is your web root.

## Customize i\_settings.php ##

  * copy i\_settings.php.dist to i\_settings.php

You must edit this file with correct paths and options

## All Done!! ##