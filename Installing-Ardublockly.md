#Installing Ardublockly

## Required Software
* [Python 2.7.x](https://www.python.org/download) (current development aims to maintain compatibility with  3.x)
* [Arduino IDE version 1.5 or higher](http://arduino.cc/en/main/software)
* Browser of your choice (currently supports Firefox, Chrome, IE10+, Opera and Safari)

#### Closure dependency
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
To run the application execute the `launch_arduino.py` file.

Your default browser should open a local web page with Ardublockly on it.