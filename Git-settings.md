**_This part of the documentation is not complete._**

# Git Settings
*Introduction still needs to be written*

## Branches
There are three permanent branches used:

### master
*Simple description still needs to be written*

### blockly-original
Mirror of the latest version of Blockly that Ardublockly is based on. This has been done to easily keep track of what version of Blockly was the last merged and compare changes, as Google does not define releases and constantly works on Head.
```
[branch "blockly-original"]
	remote = origin
	merge = refs/heads/blockly-original
```

### gh-pages
The project pages branch (http://carlosperate.github.io/ardublockly/). Currently built using the GitHub tools, but soon to be replaced with a Pelican (python static page generation) generated page instead. 
```
[branch "gh-pages"]
	remote = origin
	merge = refs/heads/gh-pages
```

This branch contains two git submodules, Ardublockly master branch and Google's Closure. This has been done to be able to demo Ardublockly online (http://carlosperate.github.io/ardublockly/ardublockly/apps/arduino_material/index.html)


## Remotes
### Upstream
Upstream points at the Google's Blockly repository
```
[remote "upstream"]
	url = https://github.com/google/blockly.git
	fetch = +refs/heads/*:refs/remotes/upstream/*
```
### _Depreciated SVN upstream_ 
Originally the Blockly repository was hosted in Googlecode using Subversion. This part of the git configuration is not longer relevant.

```
[svn-remote "svn"]
	url = http://blockly.googlecode.com/svn/
	fetch = trunk:refs/remotes/trunk
	branches = branches/*:refs/remotes/*
	tags = tags/*:refs/remotes/tags/*
```