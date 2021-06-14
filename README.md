<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# isArrayLike

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Test if a value is array-like.

<section class="installation">

## Installation

```bash
npm install @stdlib/assert-is-array-like
```

</section>

<section class="usage">

## Usage

```javascript
var isArrayLike = require( '@stdlib/assert-is-array-like' );
```

#### isArrayLike( value )

Tests if a value is [array-like][array-like].

<!-- eslint-disable object-curly-newline -->

```javascript
var bool = isArrayLike( [] );
// returns true

bool = isArrayLike( { 'length': 10 } );
// returns true
```

If provided a `string`, the function returns `true`.

```javascript
var bool = isArrayLike( 'beep' );
// returns true
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint-disable object-curly-newline, no-restricted-syntax, no-empty-function -->

<!-- eslint no-undef: "error" -->

```javascript
var isArrayLike = require( '@stdlib/assert-is-array-like' );

var bool = isArrayLike( { 'length': 10 } );
// returns true

bool = isArrayLike( [] );
// returns true

bool = isArrayLike( 'beep' );
// returns true

bool = (function test() {
    return isArrayLike( arguments );
})();
// returns true

bool = isArrayLike( null );
// returns false

bool = isArrayLike( void 0 );
// returns false

bool = isArrayLike( 5 );
// returns false

bool = isArrayLike( true );
// returns false

bool = isArrayLike( {} );
// returns false

bool = isArrayLike( function noop() {} );
// returns false
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/assert-is-array-like.svg
[npm-url]: https://npmjs.org/package/@stdlib/assert-is-array-like

[test-image]: https://github.com/stdlib-js/assert-is-array-like/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/assert-is-array-like/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/assert-is-array-like/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/assert-is-array-like?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/assert-is-array-like
[dependencies-url]: https://david-dm.org/stdlib-js/assert-is-array-like/main

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/assert-is-array-like/main/LICENSE

[array-like]: http://www.2ality.com/2013/05/quirk-array-like-objects.html

</section>

<!-- /.links -->
