# js-fixerr

Validation library for javascript

## Installation

Simply add script tag

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
