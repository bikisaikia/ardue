# Download Ardublockly-package
For an easy installation of Ardublockly there is a prepackaged version of Ardublockly (called [Ardublockly-package](https://github.com/carlosperate/ardublockly-package)) with a self-contained executable that does not have any other dependencies. You can download this version in the following links:
* [Windows](https://github.com/carlosperate/ardublockly-package)
* [Linux](https://github.com/carlosperate/ardublockly-package) (not yet ready)
* [Mac OS X](https://github.com/carlosperate/ardublockly-package) (not yet ready)

### Run Ardublockly-package
To run the application execute the `ardublockly_win.bat` file from the unzipped root folder.

Your default browser should open a local web page with Ardublockly on it.

# Installing Ardublockly
## Required Software
* [Python 2.7.x](https://www.python.org/download) (current development aims to maintain compatibility with  3.x)
* [Arduino IDE version 1.6 or higher](http://arduino.cc/en/main/software)
* [Ardublockly source code](https://github.com/carlosperate/ardublockly/archive/master.zip)
* [Closure library source code](https://github.com/google/closure-library/archive/master.zip)
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

## Closure dependency
As Ardublockly is still under development, it is currently running the uncompressed version of Blockly. This requires the [Closure library](https://developers.google.com/closure/library/) to run.

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
To download a copy of the repository, either [download this zip file](https://github.com/carlosperate/ardublockly/zipball/master) with the latest version from github, or clone locally using git:
```
git clone https://github.com/carlosperate/ardublockly.git
```
Or Subversion:
```
svn checkout https://github.com/carlosperate/ardublockly
```

## Run Ardublockly
To run the application execute the `start.py` python file.

Your default browser should open a local web page with Ardublockly on it.

