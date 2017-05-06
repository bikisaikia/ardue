# FAQs
If you have any questions not covered here, please do not hesitate to open a new issue in the [Ardublockly repository issue tracker][1].

By reporting issues we can fix them and help you to resolve them, and it will also help other users in the same situation.


## User FAQs

**Q: When I click on the settings field to change the compiler or sketch location no file browser window opens.**

**A:** Sometimes the file browser opens in the background and doesn't come into focus as expected, check all the opened windows on your desktop environment to see if this is the case.

***

**Q: I've correctly selected the Arduino IDE location in the settings, I can open the sketch in the Arduino IDE from Ardublockly, but it fails when I try to Verify or Upload the code.**

**A:** In most cases is recommended to use the latest version of the Arduino IDE, as it is less likely to have bugs that could affect Ardublockly. You can also check the [Known Arduino IDE issues](Known-Arduino-IDE-issues) article, and if your are still experiencing problems, please report it in the [Ardublockly repository issue tracker][1].

### Windows Only
**Q: I don't see any/enough/expected data from the Arduino IDE/compiler in the "Arduino IDE output" box.**

**A:** Make sure you have selected the `arduino_debug.exe` file in the settings instead of `arduino.exe`. This is because on Windows the windowed programs cannot produce console output, so the two files have been generate to allow correct console support.

***

**Q: Every time I click on verify or upload code the Arduino splash screen appears momentarily.**

**A:** Make sure you have selected the `arduino_debug.exe` file in the settings instead of `arduino.exe`.


## Developer FAQs

**Q: I have edited or created some blocks and followed the instructions to include them into Ardublockly, but I cannot see any changes.**

**A:** This could happen if your browser, or the Ardublockly desktop application, is using the old cached files. If you are using a web browser make sure you delete your cache and/or do a hard refresh, if using the desktop application you can achieve this by deleting the folder `appdata`, located inside the `arduexec` folder.

***

**Q: I've got an error message saying "Error: Closure not found".**

**A:** This could happen if you are trying to run or build the uncompressed version of Blockly and the `closure-library` folder hasn't been populated correctly. Make sure you have initialised all git submodules as indicated in the "Download the Source Code" section from the [Building Ardublockly](Building-Ardublockly#download-the-source-code) document.

***

**Q: I'm having trouble trying to build Blockly.**

**A:** Make sure you are trying to build Blockly using Python 2.7, as it is not compatible with others versions. You can find more info at the [Building Ardublockly](Building-Ardublockly#first-step-blockly) document.


[1]: https://github.com/carlosperate/ardublockly/issues