# [gulp](https://github.com/wearefractal/gulp)-traceur [![Build Status](https://travis-ci.org/sindresorhus/gulp-traceur.png?branch=master)](https://travis-ci.org/sindresorhus/gulp-traceur)

> [Traceur](https://github.com/google/traceur-compiler) is a JavaScript.next to JavaScript-of-today compiler

*Issues with the output should be reported on the Traceur [issue tracker](https://github.com/google/traceur-compiler/issues).*


## Install

Install with [npm](https://npmjs.org/package/gulp-traceur)

```
npm install --save-dev gulp-traceur
```


## Example

```js
var gulp = require('gulp');
var traceur = require('gulp-traceur');

gulp.task('default', function () {
	gulp.src('src/app.js')
		.pipe(traceur({sourceMap: true}))
		.pipe(gulp.dest('dist'));
});
```


## API

### traceur(options)

[Options](https://github.com/google/traceur-compiler/issues/584) are passed through to Traceur, except for `options.filename` which is set for you.

### traceur.RUNTIME_PATH

Absolute path to the Traceur runtime.js file.

## Output Formats

By default, Traceur treats all files as modules. This allows use of the `export`, `module` and `import` syntax.

The Traceur `modules` option allows the output module to be set to `amd` or `commonjs`.

In this way the transformer can be used to compile ES6 for AMD or NodeJS environments.

## License

[MIT](http://opensource.org/licenses/MIT) © [Sindre Sorhus](http://sindresorhus.com)
