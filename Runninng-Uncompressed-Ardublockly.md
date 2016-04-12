# Runninng Uncompressed Ardublockly Blockly

During development you could implement your changes to the source files and re-build each time (using the [Building Ardublockly](Building-Ardublockly) instructions), however the code is minified and would be quite hard to debug. For that reason it is highly encouraged to use the uncompressed version of Blockly used in Ardublockly. 

To do so, the `/ardublockly/index.html` file already contains the required sources commented out. Simply modified the following from:

```html
  <!-- Ardublockly - These three files contain the compress version -->
  <script src="../blockly/blockly_compressed.js"></script>
  <script src="../blockly/blocks_compressed.js"></script>
  <script src="../blockly/arduino_compressed.js"></script>
  <!-- To use the uncompressed version comment out the above and comment in the ones below -->
  <!--script src="../blockly/blockly_uncompressed.js"></script>
  <script src="../blockly/blocks/logic.js"></script>
  <script src="../blockly/blocks/loops.js"></script>
  <script src="../blockly/blocks/math.js"></script>
  <script src="../blockly/blocks/text.js"></script>
  <script src="../blockly/blocks/lists.js"></script>
  <script src="../blockly/blocks/colour.js"></script>
  <script src="../blockly/blocks/variables.js"></script>
  <script src="../blockly/blocks/procedures.js"></script>
  <script src="../blockly/blocks/arduino/io.js"></script>
  <script src="../blockly/blocks/arduino/map.js"></script>
  <script src="../blockly/blocks/arduino/procedures.js"></script>
  <script src="../blockly/blocks/arduino/serial.js"></script>
  <script src="../blockly/blocks/arduino/servo.js"></script>
  <script src="../blockly/blocks/arduino/spi.js"></script>
  <script src="../blockly/blocks/arduino/stepper.js"></script>
  <script src="../blockly/blocks/arduino/time.js"></script>
  <script src="../blockly/blocks/arduino/tone.js"></script>
  <script src="../blockly/blocks/arduino/variables.js"></script>
  <script src="../blockly/generators/arduino.js"></script>
  <script src="../blockly/generators/arduino/boards.js"></script>
  <script src="../blockly/generators/arduino/io.js"></script>
  <script src="../blockly/generators/arduino/lists.js"></script>
  <script src="../blockly/generators/arduino/logic.js"></script>
  <script src="../blockly/generators/arduino/loops.js"></script>
  <script src="../blockly/generators/arduino/map.js"></script>
  <script src="../blockly/generators/arduino/math.js"></script>
  <script src="../blockly/generators/arduino/procedures.js"></script>
  <script src="../blockly/generators/arduino/serial.js"></script>
  <script src="../blockly/generators/arduino/servo.js"></script>
  <script src="../blockly/generators/arduino/spi.js"></script>
  <script src="../blockly/generators/arduino/stepper.js"></script>
  <script src="../blockly/generators/arduino/text.js"></script>
  <script src="../blockly/generators/arduino/time.js"></script>
  <script src="../blockly/generators/arduino/variables.js"></script-->
```

To:

```html
  <!-- Ardublockly - These three files contain the compress version -->
  <!--script src="../blockly/blockly_compressed.js"></script>
  <script src="../blockly/blocks_compressed.js"></script>
  <script src="../blockly/arduino_compressed.js"></script-->
  <!-- To use the uncompressed version comment out the above and comment in the ones below -->
  <script src="../blockly/blockly_uncompressed.js"></script>
  <script src="../blockly/blocks/logic.js"></script>
  <script src="../blockly/blocks/loops.js"></script>
  <script src="../blockly/blocks/math.js"></script>
  <script src="../blockly/blocks/text.js"></script>
  <script src="../blockly/blocks/lists.js"></script>
  <script src="../blockly/blocks/colour.js"></script>
  <script src="../blockly/blocks/variables.js"></script>
  <script src="../blockly/blocks/procedures.js"></script>
  <script src="../blockly/blocks/arduino/io.js"></script>
  <script src="../blockly/blocks/arduino/map.js"></script>
  <script src="../blockly/blocks/arduino/procedures.js"></script>
  <script src="../blockly/blocks/arduino/serial.js"></script>
  <script src="../blockly/blocks/arduino/servo.js"></script>
  <script src="../blockly/blocks/arduino/spi.js"></script>
  <script src="../blockly/blocks/arduino/stepper.js"></script>
  <script src="../blockly/blocks/arduino/time.js"></script>
  <script src="../blockly/blocks/arduino/tone.js"></script>
  <script src="../blockly/blocks/arduino/variables.js"></script>
  <script src="../blockly/generators/arduino.js"></script>
  <script src="../blockly/generators/arduino/boards.js"></script>
  <script src="../blockly/generators/arduino/io.js"></script>
  <script src="../blockly/generators/arduino/lists.js"></script>
  <script src="../blockly/generators/arduino/logic.js"></script>
  <script src="../blockly/generators/arduino/loops.js"></script>
  <script src="../blockly/generators/arduino/map.js"></script>
  <script src="../blockly/generators/arduino/math.js"></script>
  <script src="../blockly/generators/arduino/procedures.js"></script>
  <script src="../blockly/generators/arduino/serial.js"></script>
  <script src="../blockly/generators/arduino/servo.js"></script>
  <script src="../blockly/generators/arduino/spi.js"></script>
  <script src="../blockly/generators/arduino/stepper.js"></script>
  <script src="../blockly/generators/arduino/text.js"></script>
  <script src="../blockly/generators/arduino/time.js"></script>
  <script src="../blockly/generators/arduino/variables.js"></script>
```

Keep in mind that any additional block file would have to to be added as a new `<script>` import.

Also remember to do hard refresh in-between changes to ensure your browser is not using cached old versions of the JavaScript files.