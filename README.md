<!--

@license Apache-2.0

Copyright (c) 2022 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# reSemVer

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Regular expression][mdn-regexp] to match a [semantic version][semantic-version] string.



<section class="usage">

## Usage

```javascript
import reSemVer from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-semver@v0.1.0-esm/index.mjs';
```

You can also import the following named exports from the package:

```javascript
import { REGEXP } from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-semver@v0.1.0-esm/index.mjs';
```

#### reSemVer()

Returns a [regular expression][mdn-regexp] to match a [semantic version][semantic-version] string. 

```javascript
var RE_SEMVER = reSemVer();
// returns <RegExp>

var parts = RE_SEMVER.exec( '1.0.0' );
/* returns
    [
        '1.0.0',
        '1',
        '0',
        '0',
        undefined,
        undefined,
        index: 0,
        input: '1.0.0',
        groups: undefined
    ]
*/

parts = RE_SEMVER.exec( '1.0.0-alpha.1' );
/* returns
    [
        '1.0.0-alpha.1',
        '1',
        '0',
        '0',
        'alpha',
        '1',
        index: 0,
        input: '1.0.0-alpha.1',
        groups: undefined
    ]
*/
```

#### reSemVer.REGEXP

[Regular expression][mdn-regexp] to match a [semantic version][semantic-version] string.

```javascript
var parts = reSemVer.REGEXP.exec( '0.2.3' );
/* returns
    [
        '0.2.3',
        '0',
        '2',
        '3',
        undefined,
        undefined,
        index: 0,
        input: '0.2.3',
        groups: undefined
    ]
*/
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import reSemVer from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-semver@v0.1.0-esm/index.mjs';

var RE_SEMVER = reSemVer();

var version = '1.0.0';
var bool = RE_SEMVER.test( version );
// returns true

version = '1.0.0-alpha.1';
bool = RE_SEMVER.test( version );
// returns true

version = '1.0.0-alpha.1+build.1';
bool = RE_SEMVER.test( version );
// returns true

version = '1.0.0-alpha.1+build.1.2.b8f12d7';
bool = RE_SEMVER.test( version );
// returns true

version = '1.2';
bool = RE_SEMVER.test( version );
// returns false

version = '-1.2.3';
bool = RE_SEMVER.test( version );
// returns false

version = 'a.b.c';
bool = RE_SEMVER.test( version );
// returns false

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/regexp-semver.svg
[npm-url]: https://npmjs.org/package/@stdlib/regexp-semver

[test-image]: https://github.com/stdlib-js/regexp-semver/actions/workflows/test.yml/badge.svg?branch=v0.1.0
[test-url]: https://github.com/stdlib-js/regexp-semver/actions/workflows/test.yml?query=branch:v0.1.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/regexp-semver/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/regexp-semver?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/regexp-semver.svg
[dependencies-url]: https://david-dm.org/stdlib-js/regexp-semver/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/regexp-semver/tree/deno
[umd-url]: https://github.com/stdlib-js/regexp-semver/tree/umd
[esm-url]: https://github.com/stdlib-js/regexp-semver/tree/esm
[branches-url]: https://github.com/stdlib-js/regexp-semver/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-semver/main/LICENSE

[mdn-regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

[semantic-version]: https://semver.org/

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->
