# Download Ardublockly-package
For an easy installation of Ardublockly there is a packaged version of Ardublockly with a self-contained executable that does not have any other dependencies. You can download this version in the [releases](https://github.com/carlosperate/ardublockly/releases) section of this repository.

Currently only the Windows version of the package is available, Linux and MacOS user can still use the unpackaged version.


### Run Ardublockly-package
To run the application execute the `ardublockly_win.bat` file from the unzipped root folder.

Your default browser should open a local web page with Ardublockly on it.

# Installing Ardublockly
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

