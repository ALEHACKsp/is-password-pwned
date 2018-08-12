# is-password-pwned

> Check password against pwnedpasswords.com using k-anonimity model

[![NPM version](https://badge.fury.io/js/is-password-pwned.svg)](https://www.npmjs.com/package/is-password-pwned/)
[![Build Status](https://api.travis-ci.com/commenthol/is-password-pwned.svg?branch=master)](https://travis-ci.com/commenthol/is-password-pwned)

See [Searching pwned passwords by range][].    
Caches all found hashes in LRU cache.

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### constructor

**Parameters**

-   `size` **[Number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** size of lru cache (optional, default `10000`)

**Examples**

```javascript
const Pwnd = require('is-password-pwned')
const pwnd = new Pwnd()
const num = await pwnd.get('nutella')
//> num = 20833
```

### get

get password from lru cache or request it from pwnedpasswords.com
if `num === undefined` password hash could not be found in pwnedpasswords.com

**Parameters**

-   `password` **[String](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** password to verify

Returns **await {Number}** num - number of found hashes

## Installation

Requires [nodejs](http://nodejs.org/).

```sh
$ npm install is-password-pwned
```

## Tests

```sh
$ npm test
```

## License

Unlicense https://unlicense.org

## References

- [Searching pwned passwords by range][]

[Searching pwned passwords by range]: https://haveibeenpwned.com/API/v2#SearchingPwnedPasswordsByRange