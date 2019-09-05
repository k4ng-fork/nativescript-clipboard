# NativeScript Clipboard

[![NPM version][npm-image]][npm-url]
[![Downloads][downloads-image]][npm-url]
[![Twitter Follow][twitter-image]][twitter-url]

[npm-image]:http://img.shields.io/npm/v/nativescript-clipboard.svg
[npm-url]:https://npmjs.org/package/nativescript-clipboard
[downloads-image]:http://img.shields.io/npm/dm/nativescript-clipboard.svg
[twitter-image]:https://img.shields.io/twitter/follow/eddyverbruggen.svg?style=social&label=Follow%20me
[twitter-url]:https://twitter.com/eddyverbruggen

A NativeScript plugin to copy and paste data from and to the device clipboard.

## Installation
Run the following command from the root of your project:

```
tns plugin add nativescript-clipboard
```

## Usage

> TIP: Check out the [demo app](/demo) for TypeScript examples.

To use this plugin you must first require() it:

```js
var clipboard = require("nativescript-clipboard");
```

### setText

```js
  clipboard.setText("Something relevant to put on the clipboard.").then(function() {
      console.log("OK, copied to the clipboard");
  })
```

### setTextSync
This is the synchronous version of `setText`, available since plugin version 1.2.0.

```js
  clipboard.setTextSync("Something relevant to put on the clipboard.");
```

### getText

```js
  clipboard.getText().then(function(content) {
      console.log("Read from clipboard: " + content);
  })
```

### getTextSync
This is the synchronous version of `getText`, available since plugin version 1.2.0.

```js
  var content = clipboard.getText();
  console.log("Read from clipboard: " + content);
```

## Future work
Implement support for storing data (image, etc) on the clipboard. Open an issue or PR in case you like to have that.
