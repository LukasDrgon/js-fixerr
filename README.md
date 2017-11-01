![Logo](js-fixerr.svg)
# js-fixerr  [![npm](logo.svg)](https://www.npmjs.com/package/js-fixerr) [![npm](downloads.svg)](https://www.npmjs.com/package/js-fixerr)

A Validation library for javascript

## Installation

```
npm install js-fixerr --save
```

## Usage
```
var fixerr = require('js-fixerr')
```

### [See npm docs](https://www.npmjs.com/package/js-fixerr)
>            OR

Simply add script tag
```jsx
<script type="text/javascript" src="http://apnanews.co.in/js-fixerr/js-fixerr.min.js"></script>
```

## js-fixerr Functions

- ### min
```js
  min('foobaar', 3) // true
  min('foo', 5) // false
```

- ### max
```js
  max('foobaar', 6) // true
  max('foo', 2) // false
```

- ### length
```js
  length('foobaar', 0, 7) // true
  length('foobaar', 0, 5); // false
```

- ### required
```js
  required('foobaar') // true
  required(''); // false
  required(); // false
```

- ### noWhiteSpace
```js
  noWhiteSpace('foobaar') // true
  noWhiteSpace('foo baar'); // false
```

- ### withWhiteSpace
```js
  withWhiteSpace('foo baar') // true
  withWhiteSpace('foobaar'); // false
```

- ### withSpecialChar
```js
  withSpecialChar('foo@$ba%ar') // true
  withSpecialChar('f!oo~ar') // true
  withSpecialChar('foobaar'); // false
```

- ### noSpecialChar
```js
  noSpecialChar('foobaar') // true
  noSpecialChar('f!oo~ar') // false
  noSpecialChar('foo@ba^ar'); // false
```

- ### lower
```js
  lower('foobaar') // true
  lower('fooBaar') // false
  lower('Foobaar'); // false
```

- ### upper
```js
  upper('FOOBAAR') // true
  upper('fooBaar') // false
  upper('Foobaar'); // false
```

- ### string
```js
  string('FOOBAAR') // true
  string('foobaar') // true
  string(1233) // false
```

- ### number
```js
  number(12131) // true
  number('foobaar') // false
```

- ### noAlphaNumeric
```js
  noAlphaNumeric('foobaar') // true
  noAlphaNumeric('fooba901') // false
```

- ### mobile
```js
  mobile(1234567890) // true
  mobile(745387) // false
```

- ### email
```js
  email('jsfixerr@gmail.com') // true
  email('jsfixerr@com') // false
  email('jsfix err@ gmail com') // false
```

- ### date
```js
  date('10/12/2017') // true
  date('10-12-2017') // true
  date('16/34/3434') //false
```

- ### array
```js
  array([23,23,90]) // true
  array('[12,23,546]') // false
  array(['a','b','c']) // true
```

- ### isInteger
```js
  isInteger(23) // true
  isInteger('12') // false
  isInteger('a') // false
```

- ### isFloat
```js
  isFloat(23.12) // true
  isFloat('12') // false
  isFloat(34) // false
```
- ### vowel
```js
  vowel('a') // true
  vowel('aeo') // true
  vowel('aeoiu') // true
  vowel('sdf') // false
  vowel('sdfa') // false
```

- ### isIdExists
```js
  <h2 id="title"></h2>
    isIdExists('title') // true
    isIdExists('head') // false
```

- ### isClassExists
```js
  <h2 class="title"></h2>
    isClassExists('title') // true
    isClassExists('head') // false
```

- ### isTagExists
```js
  <h2></h2>
    isTagExists('h2') // true
    isTagExists('h5') // false
```

