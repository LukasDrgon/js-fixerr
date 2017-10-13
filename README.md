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
