**_This part of the documentation is not yet complete._**

# Git Settings
*Introduction still needs to be written*

## Branches
There are 2 permanent branches used, any other branch would be a feature branch meant to be merged into master once it is finished.

### master branch
Where the latest working version of the Ardublockly source code resides.

### gh-pages branch
The project pages branch [http://carlosperate.github.io/ardublockly/](http://carlosperate.github.io/ardublockly/) contains a general project introduction page and an offers online accessibility to the Ardublockly front end web-based part of the application [http://carlosperate.github.io/ardublockl/ardublockly/](http://carlosperate.github.io/ardublockly/ardublockly/).

```
[branch "gh-pages"]
	remote = origin
	merge = refs/heads/gh-pages
```

This branch contains two git submodules, Ardublockly master branch and Google's Closure. This has been done to be able to demo Ardublockly online (http://carlosperate.github.io/ardublockly/ardublockly/apps/arduino_material/index.html)

## Remotes
### blockly
The `blockly` remote points at the Google's Blockly repository, so that the latest updates can be pulled in.

```
[remote "upstream"]
	url = https://github.com/google/blockly.git
	fetch = +refs/heads/*:refs/remotes/upstream/*
```

#### _Depreciated SVN upstream_ 
Originally the Blockly repository was hosted in Googlecode using Subversion. This part of the git configuration is not longer relevant.

```
[svn-remote "svn"]
	url = http://blockly.googlecode.com/svn/
	fetch = trunk:refs/remotes/trunk
	branches = branches/*:refs/remotes/*
	tags = tags/*:refs/remotes/tags/*
```


## Git Subtrees
There a single subtree in this repository to contain a fork of Google's Blockly. This fork contains additional features as part of Ardublockly that need to be maintained.

Once the subtree is configure, to pull the latest updates from remote blockly the following commands can be used from the project root directory:

```
git fetch blockly master
git subtree pull --prefix blockly blockly master
```


## Git Submodules
There are two submodules as part of this repository, the [Google's Closure library](https://github.com/google/closure-library/) and [PyInstaller](www.pyinstaller.org) Python package.

To initialise the modules after a git clone the following command should be executed. From the project root directory:

```
git submodule update --init --recursive
```
