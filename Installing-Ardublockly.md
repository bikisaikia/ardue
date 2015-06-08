# Install Ardublockly

There are two ways to run Ardublockly.

a) Download the "packaged version": Simplest method, download a zip file which contains the Ardublockly executable software.

b) Download the "development version": Requires Python and a browser (like Chrome or Firefox).


## Install packaged Ardublockly
The easiest way to use Ardublockly is to download the packaged version, which is a self-contained program that does not have any other dependencies (other than having the Arduino IDE installed).

You can download the latest stable version in the [releases](https://github.com/carlosperate/ardublockly/releases) section of this repository.

At the moment there is no first release, but development builds can be found in the link below. The Windows version works in both 32 and 64 bit of windows 7 and 8 (haven't had a chance to test it in older version, please let me know if you have), I'm currently working over some issues on Linux, and the Mac build is imminent. For the temporarily unsupported platform the "development version" works on all operating systems.

http://ardublockly-builds.s3-website-us-west-2.amazonaws.com/index.html


### Run the packaged Ardublockly
To run the application execute the `ardublockly_run` batch or bash file located on the the root of the Ardublockly folder.

Your default browser should open a local web page to load the Ardublockly application.

The Arduino IDE is requied to load the programs into an Arduino board, more information can be found in the [Configure Ardublockly page](https://github.com/carlosperate/ardublockly/wiki/Configure-Ardublockly).


## Install development Ardublockly
The version of Ardublockly is the main is the development environment for the application. You can easily run the latest versions and updates using this method and 

## Required Software
* [Python 2.7.x](https://www.python.org/download) (current development aims to maintain compatibility with  3.x)
* [Arduino IDE version 1.6 or higher](http://arduino.cc/en/main/software)
* [Ardublockly source code](https://github.com/carlosperate/ardublockly/archive/master.zip)
* Modern browser of your choice (currently supports Firefox, Chrome, IE10+, Opera and Safari)

#### Linux only requirement
Tkinter, which is used in Ardublockly, is not part of standard python on Linux and needs to be installed.

Install Tkinter for Python 2 on Ubuntu:
```
sudo apt-get install python-tk
```
OR, install Tkinter for Python 3 on Ubuntu:
```
sudo apt-get install python3-tk
```

## Git Submodule
As Ardublockly is still under development, it is currently running the uncompressed version of Blockly. This requires the [Closure library](https://developers.google.com/closure/library/) to run, which has been included in this repository as a git submodule.

To download a copy of the repository, either [download this zip file](https://github.com/google/closure-library/archive/master.zip) with the latest version from github, or clone locally using git:
```
git clone https://github.com/google/closure-library.git

```
Or Subversion:
```
svn checkout https://github.com/google/closure-library
```
The folder containing the library must be named `closure-library` and be located in the same directory than the `Ardublockly` folder.

More info on the Closure requirement can be found in the [Blockly documentation](https://developers.google.com/blockly/hacking/closure).

## Downloading Ardublockly
To download a working copy of the repository you'll have clone locally using git:
```
git clone https://github.com/carlosperate/ardublockly.git
cd ardublockly
git submodule update --init --recursive
```

When the repository is downloaded [directly from github as zip file](https://github.com/carlosperate/ardublockly/zipball/master), the internal git submodule is not pull with it, which is why git is the best method to download a working copy.

If for some reason you unable to use git, you can download [Ardublockly from github as zip file](https://github.com/carlosperate/ardublockly/zipball/master), download [Closure library as a zip file](https://github.com/google/closure-library/archive/master.zip) and then uncompress the contents from the Ardublockly zip file and then unzip the Closure library into the `closure-library` folder within Ardublockly (make sure there is not an additional "closure-library" nested folder inside this one).


## Run Ardublockly
To run the application execute the `start.py` python file.

Your default browser should open a local web page with Ardublockly on it.

