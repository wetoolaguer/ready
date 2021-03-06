# ready

[![Version Badge][version-image]][project-url]
[![Build Status][build-image]][build-url]
[![Dependencies][dependencies-image]][project-url]
[![License][license-image]][license-url]
[![File Size][file-size-image]][project-url]

> Watch for specific element availability on initial page load as well as dynamically appended elements via mutation observers. Please refer to the [blog post](http://www.ryanmorr.com/using-mutation-observers-to-watch-for-element-availability) to read more.

## Usage

Provide a selector string for the element(s) you want to target as the first argument and a callback function as the second argument. It returns a function that stops observing for new elements only for that particular selector/callback combination:

``` javascript
const off = ready('.foo', (element) => {
    off(); // Stop observing for .foo elements
});
```

When any element matching the selector becomes available, the callback is invoked in the context of the element as well as passing it as the only parameter. If multiple elements are found, the callback is invoked in succession for each element in document order.

## Installation

Ready is [CommonJS](http://www.commonjs.org/) and [AMD](https://github.com/amdjs/amdjs-api/wiki/AMD) compatible with no dependencies. You can download the [development](https://github.com/ryanmorr/ready/raw/master/dist/ready.js) or [minified](https://github.com/ryanmorr/ready/raw/master/dist/ready.min.js) version, or install it in one of the following ways:

``` sh
npm install ryanmorr/ready

bower install ryanmorr/ready
```

## Tests

Open `test/runner.html` in your browser or test with PhantomJS by issuing the following commands:

``` sh
npm install
npm install -g gulp
gulp test
```

## License

This project is dedicated to the public domain as described by the [Unlicense](http://unlicense.org/).

[project-url]: https://github.com/ryanmorr/ready
[version-image]: https://badge.fury.io/gh/ryanmorr%2Fready.svg
[build-url]: https://travis-ci.org/ryanmorr/ready
[build-image]: https://travis-ci.org/ryanmorr/ready.svg
[dependencies-image]: https://david-dm.org/ryanmorr/ready.svg
[license-image]: https://img.shields.io/badge/license-Unlicense-blue.svg
[license-url]: UNLICENSE
[file-size-image]: https://badge-size.herokuapp.com/ryanmorr/ready/master/dist/ready.min.js.svg?color=blue&label=file%20size