Tipsy Source
===================

Getting Started
---------------
To get started with the Tipsy sources, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/version-control.html).


Create the Directories
----------------------

You will need to set up some directories in your build environment.

To create them run:

    mkdir -p ~/bin
    mkdir -p ~/tipsy


Install the Repository
----------------------

Enter the following to download the "repo" binary and make it executable:

curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo && chmod a+x ~/bin/repo

You may need to reboot for these changes to take effect.
Now enter the following to initialize the repository:

    cd ~/tipsy


Repositories:
---------------

Before you continue --> run this in the terminal
----------------------------------------
    repo init -u https://github.com/TipsyOs/manifest.git -b 10.0 && repo sync -f

*PLEASE NOTE THAT YOU MUST USE THE -f flag when repo syncing/initializing if you want to sync with our default -j8 setup as android.googlesource seems to like to reject your requests if you set your -jflag too high.
if you wish to avoid this issue run it repo sync -j1 otherwise -f (force) is recommended so it will resync the repos it gets error codes on. Thank you and have a nice day.*


Building the System
---------------

Please note that if you are building on Mac OS X, you are required to install coreutils from MacPorts before you continue.
Initialize the environment with the envsetup.sh script. Note that replacing "source" with a single dot saves a few characters, and the short form is more commonly used in documentation.

    . build/envsetup.sh
    lunch

Enter the number of the build you want to start and press enter

Build the Code:

    make tipsy -j8 (or as many threads your hardware can handle)
