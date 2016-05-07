# Install Ardublockly

There are two ways to run Ardublockly.

a) Run the executable application: Simplest method, download a zip file which contains the pre-packaged Ardublockly executable software.

b) Run the "core version": Running from source code, requires only Python and a browser (like Chrome or Firefox).

Both these methods can be run from the "pre-packaged" download, and the GitHub repository source code.


## Install packaged Ardublockly
The easiest way to use Ardublockly is to download the packaged version, which is a self-contained application that does not have any other dependencies (other than having the Arduino IDE installed).

You can download the latest stable version in the [releases](https://github.com/carlosperate/ardublockly/releases) section of this repository.

#### Development builds of packaged Ardublockly
Additionally, development builds with the latest features still under development can be found in the links below. The Windows version works in both 32 and 64 bit of windows 7 and higher. The Linux version works only on x64, built on Ubuntu 12.04. The Mac OS X version works on 10.8 Mountain Lion or higher.

http://ardublockly-builds.s3-website-us-west-2.amazonaws.com/index.html

| Linux build         | Windows build       | Mac OS X build       |
|:-------------------:|:-------------------:|:--------------------:|
| [![Linux Build Status](https://circleci.com/gh/carlosperate/ardublockly/tree/master.svg?style=svg)](https://circleci.com/gh/carlosperate/ardublockly/tree/master) | [![Windows Build status](https://ci.appveyor.com/api/projects/status/t877g920hdiifc2i?svg=true)](https://ci.appveyor.com/project/carlosperate/ardublockly) | [![Mac Build Status](https://travis-ci.org/carlosperate/ardublockly.svg?branch=master)](https://travis-ci.org/carlosperate/ardublockly) |
| [Download Link](http://ardublockly-builds.s3-website-us-west-2.amazonaws.com/index.html?prefix=linux/) | [Download Link](http://ardublockly-builds.s3-website-us-west-2.amazonaws.com/index.html?prefix=windows/) | [Download Link](http://ardublockly-builds.s3-website-us-west-2.amazonaws.com/index.html?prefix=mac/)  |

For any these and other platforms, the "core version" should work on all operating systems with Python and a modern web browser. 


### Run the packaged Ardublockly
To run the application the steps are slightly different depending on the platform.

* __Windows__: Double click on the `ardublockly_run.bat` file located on the Ardublockly folder.
* __Linux__: Execute the `ardublockly_run.sh` shell script located on the Ardublockly folder.
* __OS X__: Right click the `Ardublockly.app` file and click `open`.

![Ardublockly desktop application](http://carlosperate.github.io/ardublockly/images/screenshot_desktop_1.png)

The Arduino IDE is required to compile and load the programs into an Arduino board, more information can be found in the [Configure Ardublockly page](https://github.com/carlosperate/ardublockly/wiki/Configure-Ardublockly).


## Install from Ardublockly source code
Often referred as the "core version" of Ardublockly, this version is the main development environment for the application. You can easily run the latest updates using this method, and should still be able to work if there is an issue with the packed Ardublockly software on your environment. 

### Required Software
* [Python 2.7.x](https://www.python.org/download): Ardublockly is maintains compatibility with 3.x, but is mainly developed using Python 2
* [Arduino IDE version 1.6 or higher](http://arduino.cc/en/main/software): The latest version is always recommended
* Modern browser of your choice: Currently supports Firefox, Chrome, IE10+, Opera and Safari; Chrome is recommended
* Ardublockly source code: The "Downloading Ardublockly" section details how to obtain it
* [Git](https://git-scm.com/downloads): It is not strictly required for downloading the source code, but it simplifies the process

#### Linux only requirement
Tkinter, which is used in Ardublockly, is not always part of standard Python environment on Linux and needs to be installed.

Install Tkinter for Python 2 on Ubuntu:

```
sudo apt-get install python-tk
```

OR, install Tkinter for Python 3 on Ubuntu:

```
sudo apt-get install python3-tk
```

### Downloading Ardublockly
The easiest way to download a working copy of the repository is using git:

```
git clone https://github.com/carlosperate/ardublockly.git
cd ardublockly
git submodule update --init --recursive
```

When the repository is downloaded [directly from github as zip file](https://github.com/carlosperate/ardublockly/zipball/master), the internal git submodules are not included, which is why git is the best method to download a working copy.

##### Download without git
If for some reason you are unable to use git, you can download [Ardublockly from GitHub as zip file](https://github.com/carlosperate/ardublockly/zipball/master) and the [Closure library as a zip file](https://github.com/google/closure-library/archive/master.zip). Uncompress the contents from the Ardublockly zip file and then unzip the Closure library into the `closure-library` folder within Ardublockly (make sure there is not an additional "closure-library" nested folder inside this one).

If you also need to build Ardublockly locally (which is not necessary to run the development version), all the git submodules required are listed in the [.gitmodules file in the repository](https://github.com/carlosperate/ardublockly/blob/master/.gitmodules).


### Run Ardublockly from source code
To run the "core version" execute the `start.py` python script file located on the the root of the Ardublockly folder (this also works on the "packaged" Ardublockly version):

```
python start.py
```

Your default browser should open a local web page to load the Ardublockly application.

![Ardublockly development](http://carlosperate.github.io/ardublockly/images/screenshot_browser_1.png)

The Arduino IDE is required to compile and load the programs into an Arduino board, more information can be found in the [Configure Ardublockly page](https://github.com/carlosperate/ardublockly/wiki/Configure-Ardublockly).

#### Run the full Ardublockly desktop application from source
To run the full desktop version of the development Ardublockly you will also need to install [node.js](https://nodejs.org/).

Navigate to the `electron` folder inside the `package` directory:

```
cd package\electron
```

Execute the following command to download all the dependencies required to for the desktop application, this might take a while:

```
npm install
```

Once that's done, run the following command to open the desktop application:

```
npm start
```

The Arduino IDE is still required to compile and load the programs into an Arduino board, more information can be found in the [Configure Ardublockly page](https://github.com/carlosperate/ardublockly/wiki/Configure-Ardublockly).