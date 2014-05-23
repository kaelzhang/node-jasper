# minicry [![NPM version](https://badge.fury.io/js/minicry.svg)](http://badge.fury.io/js/minicry) [![Build Status](https://travis-ci.org/kaelzhang/node-minicry.svg?branch=master)](https://travis-ci.org/kaelzhang/node-minicry) [![Dependency Status](https://gemnasium.com/kaelzhang/node-minicry.svg)](https://gemnasium.com/kaelzhang/node-minicry)

Minicry is an elegant template engine.

## Install

index.minicry
```html
html
  body
    facade abc
```

## Usage

```js
var minicry = require('minicry');
minicry.register('facade', function(name){
  return '<script>facade({mod: "' + name + '"});</script>';
});

minicry.compile(fs.readFileSync('index.minicry'));
```

```html
<html>
  <body>
    <script>facade({mod: "abc"})</script>
  </body>
</html>
```

## Licence

MIT
<!-- do not want to make nodeinit to complicated, you can edit this whenever you want. -->