# Install Ardublockly

There are two ways to run Ardublockly.

a) Download the "packaged version": Simplest method, download a zip file which contains the Ardublockly executable software.

b) Download the "development version": Requires Python and a browser (like Chrome or Firefox).


## Install packaged Ardublockly
The easiest way to use Ardublockly is to download the packaged version, which is a self-contained program that does not have any other dependencies (other than having the Arduino IDE installed).

You can download the latest stable version in the [releases](https://github.com/carlosperate/ardublockly/releases) section of this repository.

At the moment there is no first release, but development builds can be found in the link below. The Windows version works in both 32 and 64 bit of windows 7 and 8 (haven't had a chance to test it in older version, please let me know if you have), I'm currently working over some issues on Linux, and the Mac build is imminent after that.

http://ardublockly-builds.s3-website-us-west-2.amazonaws.com/index.html

For the temporarily unsupported platforms, the "development version" works on all operating systems.


### Run the packaged Ardublockly
To run the application execute the `ardublockly_run` batch or bash file located on the the root of the Ardublockly folder.

![Ardublockly desktop application](https://carlosperate.github.io/ardublockly/images/screenshot_desktop_1.png)

The Arduino IDE is required to load the programs into an Arduino board, more information can be found in the [Configure Ardublockly page](https://github.com/carlosperate/ardublockly/wiki/Configure-Ardublockly).


## Install development Ardublockly
This version of Ardublockly is the main development environment for the application. You can easily run the latest versions and updates using this method, and should be able to work if there is an issue with the packed Adublockly on your computer. 

### Required Software
* [Python 2.7.x](https://www.python.org/download): Ardublockly is designed to maintain compatibility with 3.x, but is mainly developed using Python 2
* [Arduino IDE version 1.6 or higher](http://arduino.cc/en/main/software): Due to the significant changes brought by versions 1.5 and 1.6 it is recommended to use the latest available
* Modern browser of your choice: Currently supports Firefox, Chrome, IE10+, Opera and Safari
* Ardublockly source code: The "Downloading Ardublockly" section details how to obtain it
* [Git](https://git-scm.com/downloads): It is not strictly required for downloading the source code, but it simplifies the process

#### Linux only requirement
Tkinter, which is used in Ardublockly, is not part of standard Python environment on Linux and needs to be installed.

Install Tkinter for Python 2 on Ubuntu:

```
sudo apt-get install python-tk
```

OR, install Tkinter for Python 3 on Ubuntu:

```
sudo apt-get install python3-tk
```

### Downloading Ardublockly
To download a working copy of the repository the easiest way is to clone locally using git:

```
git clone https://github.com/carlosperate/ardublockly.git
cd ardublockly
git submodule update --init --recursive
```

When the repository is downloaded [directly from github as zip file](https://github.com/carlosperate/ardublockly/zipball/master), the internal git submodules are not included, which is why git is the best method to download a working copy.

##### Download without git
If for some reason you unable to use git, you can download [Ardublockly from github as zip file](https://github.com/carlosperate/ardublockly/zipball/master) and the [Closure library as a zip file](https://github.com/google/closure-library/archive/master.zip). Uncompress the contents from the Ardublockly zip file and then unzip the Closure library into the `closure-library` folder within Ardublockly (make sure there is not an additional "closure-library" nested folder inside this one).

If you also need to build Ardublockly locally (which is not necessary to run the development version), all the git submodules required are listed in the [.gitmodules file in the repository](https://github.com/carlosperate/ardublockly/blob/master/.gitmodules).


### Run Ardublockly
To run the development version execute the `start.py` python script file located on the the root of the Ardublockly folder (this also works on the "packaged" Ardublockly version):

```
python start.py
```

Your default browser should open a local web page to load the Ardublockly application.

![Ardublockly development](https://carlosperate.github.io/ardublockly/images/screenshot_browser_1.png)

The Arduino IDE is required to load the programs into an Arduino board, more information can be found in the [Configure Ardublockly page](https://github.com/carlosperate/ardublockly/wiki/Configure-Ardublockly).
