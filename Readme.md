# minify

Super clean API for minifying Javascript, HTML or CSS.

So you don't have to keep googling for the right tool or the tool’s API. And so that you get a nice CLI regardless.

This is [Harp](https://github.com/sintaxi/harp)’s fork, which is nearly identical to [the original](https://github.com/ianstormtaylor/minify). The differences are:

- It’s published to npm, to remove the dependency on GitHub for installing
- It has more up-to-date dependencies
- It has npm run scripts for development

## Installation

```sh
npm install harp-minify
```

## CLI

```
Usage: minify [<input>] [<output>]

Options:

  -h, --help     output usage information
  -V, --version  output the version number

Examples:

  # pass an input and output file
  $ minify input.css output.css

  # use stdin and stdout
  $ cat input.css | myth | minify > output.css
```

## Node

```javascript
var minify = require('minify');

// choose javascript, html or css
var js = minify.js('js string');
var html = minify.html('html string');
var css = minify.css('css string');

// or pass an unknown string
var min = minify('unknown string');
```

When using JavaScript, you may also alter the default options using the same API as [UglifyJS](https://github.com/mishoo/UglifyJS2):


```javascript
var js = minify.js('js string', {
  compress: false,
  mangle: false
});
```

## License

The MIT License (MIT) => Apache-2.0 from 2016

Copyright © 2013–2015, Ian Storm Taylor &lt;ian@ianstormtaylor.com&gt;<br/>Copyright © 2015 [Chloi Inc.](http://chloi.io)&gt;<br/>Copyright © 2016-2019 [Frank Lemanschik](https://dspeed.eu) 


