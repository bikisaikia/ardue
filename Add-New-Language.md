# Adding a New Language to Ardublockly
_(Work in Progress: This page should describe how to add new languages to Ardublockly)_

While Blockly has been translated to a large number of languages using TranslateWiki (more info [here](https://developers.google.com/blockly/hacking/translating)), only a small subset of these translations has been expanded to cover the additional blocks and user interface text from Ardublockly.

In essence there are two files that will need to be updated/created to add a new Language:
* `blockly/msg/json/<your_language_file>.json`: This existing file contains the Blockly strings. _(Need to expand this to indicate which strings to include)_
* `ardublockly/msg/<new_file_for_your_language>.js`: A new file will have to be created and updated to include the translated text for the user interface. A "base version" of this file can just be a copy-paste of `ardublockly/msg/en.js`.

After that, Blockly needs to be built to convert the Blockly JSON strings into JavaScript variables that can be used by the blocks. To do this, from the `blockly` folder on a terminal:

```
python build.py
```

_(Mention that Blockly doesn't neccesarily have to be built and that just sending a PR with those two files should be fine)_

_(Mention that the front end js file can be updated to include the new language on the settings menu.)_

_(Indicate how to send a PR)_