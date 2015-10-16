# Asterisk Voicemail for iPhone #
Copyright 2008 Chris Carey (http://chriscarey.com).
This program is distributed under the terms of the GNU General Public License

## Contact ##
Contact me at **chris.carey @ gmail.com** if you need assistance.

## Development Change Log ##

### 2008-09-23 (v0.13 release) ###

  * Changed listen link to listen.php, removing the need for Apache Alias
  * Added g\_debug\_path. Debug path was hard coded which caused crash if not exist.

### 2008-09-22 (v0.12 release) ###

The main thing to mention about this release is that it is the easiest yet to install. Everything is included in the zip file. Unzip, configure i\_settings.php, configure Apache, and GO!

You may notice that the Installation Guide is significantly smaller now.

  * Backed off the 'embed' of sound files into the page. It never worked that well. Now with iPhone firmware 2.0, the quicktime automagically exits after playing the sound file.
  * Added Icons
  * Fixed PHP4 complaint about & in my loops
  * Started on prerequisite check in check.php
  * Include preconfigured Smarty
  * Include a preconfigured iUI
  * Moved smarty templates to smarty/templates
  * Add a ? after listen link. This seems to make more phones happy

### 2008-04-05 (v0.10 release) ###

  * Embedding mp3 instead of linking to it. This is a much better integration. No longer have to hit the back button after listening to messages to jump back from quicktime to the browser.
  * Some graphics updates. Added some asterisk logos
  * clear whitespace at the end of i\_settings.php - which is causing a "headers already sent' error
  * Handle voicemail.conf => issue. Filter out the > then parse by =, so we handle both styles (also test with spaces around = and no spaces.
  * if debug.txt doesnt exist, create it.
  * fix doSendFileWithResume() with SML's fixes

### 2008-03-15 (v0.09 release) ###
  * Font and color changes
  * Clean up the about page
  * Fixed MySQL authentication
  * Fixed the security hole!! Now supports streaming mp3 audio to the phone through a PHP page where security checks can be performed. Check the Installation Guide for updated Apache instructions.
  * Reorganize the i\_settings.php file. Added g\_secret\_salt. You will need to grab a copy of the new i\_settings.php.dist file and overwrite your own. And, of course, you will need to configure the new file.

### 2008-03-08 (v0.08 release) ###
  * DeleteMessages function was missing. Delete is now working
  * Move Messages is now working
  * Fixed Reindex Messages function

### 2008-03-08 (v0.07 release) ###
  * Made Message Detail screen look better
  * Made a little more progress on "Move Message" code.

### 2008-03-07 (v0.06 release) ###
  * After loading the code on my MySQL based server I found some DB bugs.
  * Added a new i\_setting for Smarty. Some people have the class file elsewhere.

### 2008-03-07 (v0.05 release) ###
  * Added Check for Updates
  * Added GUI for "Move Message" support
  * Cleaned up code in index.php and main.php a lot
  * Moved "g\_default\_prefix" to i\_settings.php. You must copy a new i\_settings.php.dist for this version

### 2008-03-06 (v0.04 release) ###
  * Added preliminary support for Settings screen. It will now load name, pass, email from MySQL or voicemail.conf

### 2008-03-05 (v0.03 release) ###
  * Prepared for posting on Google Code

### 2008-03-04 (v0.02 release) ###
  * Write preliminary function for voicemail.conf authentication

### 2008-03-03 (v0.01 release) ###
  * Prepare code for release
  * Write stub function for voicemail.conf authentication

### 2008-02-25 ###
  * Added "Settings" back, and Added "Move Messages" button. Both of these features are non-functional at this time.
  * Cleaned up date format on Message Detail, and changed it's font size back up to normal

### 2008-02-24 ###
  * Added Cookie Support
  * Renamed "Check Messages" to "Messages"
  * Displaying "Saved" messages
  * Added ChangeLog
  * Updated About page with email link
  * Removed "Settings" page until I get it working
  * Allow 7 digit logins, will prepend a default prefix
  * Disabled iPhone's "format detection" for phone numbers
