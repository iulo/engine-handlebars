# engine-handlebars [![NPM version](https://badge.fury.io/js/engine-handlebars.svg)](http://badge.fury.io/js/engine-handlebars)

> Handlebars engine, consolidate.js style but with enhancements. This works with Assemble, express.js, engine-cache or any application that follows consolidate.js conventions.

## Install with [npm](npmjs.org)

```bash
npm i engine-handlebars --save
```

## Usage

```js
var handlebars = require('engine-handlebars');
```

## API
### [.compile](index.js#L37)

Handlebars string support. Compile the given `str` and register helpers and partials from settings

* `str` **{String}**    
* `settings` **{Object}**: object containing optional helpers and partials    

```js
var engine = require('engine-handlebars');
var fn = engine.compile('{{name}}', {});
```

### [.render](index.js#L67)

Handlebars string support. Render the given `str` and invoke the callback `cb(err, str)`.

* `str` **{String|function}**    
* `context` **{Object|Function}**: or callback.    
* `cb` **{Function}**: callback function.    

```js
var engine = require('engine-handlebars');
engine.render('{{name}}', {name: 'Jon'}, function (err, content) {
  console.log(content); //=> 'Jon'
});
```

### [.renderSync](index.js#L99)

Synchronously render Handlebars templates.

* `str` **{Object|Function}**: The string to render or compiled function.    
* `context` **{Object}**    
* `returns` **{String}**: Rendered string.  

```js
var engine = require('engine-handlebars');
engine.renderSync('<%= name %>', {name: 'Jon'});
//=> 'Jon'
```

### [.renderFile](index.js#L127)

Handlebars file support. Render a file at the given `path` and callback `cb(err, str)`.

* `path` **{String}**    
* `options` **{Object|Function}**: or callback function.    
* `cb` **{Function}**: callback function    

```js
var engine = require('engine-handlebars');
engine.renderSync('foo/bar/baz.tmpl', {name: 'Jon'});
//=> 'Jon'
```


## Author

**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2014-2015 Jon Schlinkert  
Released under the MIT license

***

_This file was generated by [verb](https://github.com/assemble/verb) on February 02, 2015._


[delims]: https://github.com/jonschlinkert/delims "template delimiters"