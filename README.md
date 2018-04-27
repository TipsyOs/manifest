Welcome to TipsyOs
===================

This is a frunk ground. Make sure u're drunk enough to build this.

Getting Drunk:
---------------

To get started with Tipsy, you'll need to get familiar with
[Git and Repo](http://source.android.com/download/using-repo).

To initialize your local repository using the TipsyOs trees, use this command:


	repo init -u git://github.com/TipsyOs/platform_manifest.git -b 8.1


Then sync up with this command:

	repo sync -f

	(once your local manifest is added for devices, or once u have brunched an official device; u may need to force the sync a bit by using $ repo sync --force-sync command)


Your device is properly lunched? Build the Drunkness!
-----------------------------------------------------
```
make tipsy -j#
```
Have Fun and stay Tipsy!!
-----------------------
