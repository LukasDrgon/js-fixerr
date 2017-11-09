![Logo](js-fixerr.svg)[](https://www.npmjs.com/package/js-fixerr)
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


  - min
  - max
  - length
  - required
  - noWhiteSpace
  - withWhiteSpace
  - withSpecialChar
  - noSpecialChar
  - lower
  - upper
  - string
  - number
  - noAlphaNumeric
  - mobile
  - email
  - date
  - array
  - isInteger
  - isFloat
  - vowel
  - isPrime
  - isVideoUrl
  - isPositiveInteger
  - isEven
  - isOdd
  - isMacAddress
  - isleapYear
  - isIPaddress
  - factors
  - factorial
  - hasVowel
  - isPerfectSquare
  - isBoolean
  - isRoman
  - isAge

### min 
*Validate if the input is smaller then the min value*
```jsx
  min('foobaar', 3) // return true
  min(34563, 4) // return true
  min(345, 4) // return false
  min('foo', 5) // return false
```

### max
*Validate if the input is greater then the max value*
```jsx
  max('foobaar', 6) // return true
  max(12345, 6) // return true
  max(12345, 3) // return false
  max('foo', 2) // return false
```

### length
*Validate if the string lie between the given value*
```jsx
  length('foobaar', 0, 7) // return true
  length(123456, 0, 7) // return true
  length(123456567878, 0, 7) // return flase
  length('foobaar', 0, 5); // return false
```

### required
*Validate if the input is empty*
```jsx
  required('foobaar') // return true
  required(''); // return false
  required(' '); // return false
  required(); // return false
```

### noWhiteSpace
*Validate if the input has no whitespace*
```jsx
  noWhiteSpace('foobaar') // return true
  noWhiteSpace(' ') // return false
  noWhiteSpace('') // return false
  noWhiteSpace('foo baar'); // return false
```

### withWhiteSpace
*Validate if the input has whitespace*
```jsx
  withWhiteSpace('foo baar') // return true
  withWhiteSpace('') // return false
  withWhiteSpace(' ') // return true
  withWhiteSpace('foobaar'); // return false
```

### withSpecialChar
*Validate if the input has Special character*
```jsx
  withSpecialChar('foo@$ba%ar') // return true
  withSpecialChar('f!oo~ar') // return true
  withSpecialChar(' ') // return true
  withSpecialChar('foobaar'); // return false
```

### noSpecialChar
*Validate if the input has no Special character*
```jsx
  noSpecialChar('foobaar') // return true
  noSpecialChar('f!oo~ar') // return false
  noSpecialChar('foo@ba^ar'); // return false
```

### lower
*Validate if the input is in lower case*
```jsx
  lower('foobaar') // return true
  lower('fooBaar') // return false
  lower('Foobaar'); // return false
```

### upper
*Validate if the input is in upper case*
```jsx
  upper('FOOBAAR') // return true
  upper('fooBaar') // return false
  upper('Foobaar'); // return false
```

### string
*Validate if the input is a string*
```jsx
  string('FOOBAAR') // return true
  string('foobaar') // return true
  string(1233) // return false
```

### number
*Validate if the input is a number*
```jsx
  number(12131) // return true
  number('foobaar') // return false
```

### noAlphaNumeric
*Validate if the input has no Alphanumeric characters*
```jsx
  noAlphaNumeric('foobaar') // return true
  noAlphaNumeric('fooba901') // return false
```

### mobile
*Validate if the input is a 10 digit mobile number*
```jsx
  mobile(1234567890) // return true
  mobile(745387) // return false
```

### email
*Validate if the input is a email address*
```jsx
  email('jsfixerr@gmail.com') // return true
  email('jsfixerr@com') // return false
  email('jsfix err@ gmail com') // return false
```

### date
*Validate if the input is a date*
```jsx
  date('10/12/2017') // return true
  date('10-12-2017') // return true
  date('16/34/3434') //return false
```

### array
*Validate if the input is a array*
```jsx
  array([23,23,90]) // return true
  array('[12,23,546]') // return false
  array(['a','b','c']) // return true
```

### isInteger
*Validate if the input is a Integer*
```jsx
  isInteger(23) // return true
  isInteger('12') // return false
  isInteger('a') // return false
```

### isFloat
*Validate if the input is a Float*
```jsx
  isFloat(23.12) // return true
  isFloat('12') // return false
  isFloat(34) // return false
```
### vowel
*Validate if the input is a vowel*
```jsx
  vowel('a') // return true
  vowel('aeo') // return true
  vowel('aeoiu') // return true
  vowel('sdf') // return false
  vowel('sdfa') // return false
```

### isPrime
*Validate if the input is a prime number*
```jsx
  isPrime(7) // return true
  isPrime(12) // return false
```

### isVideoUrl
*Validate if the input is a youtube video Url*
```jsx
  isVideoUrl('https://www.youtube.com/watch?v=LyrqhruLhBA') // return true
  isVideoUrl('https://www.youtube.com/watch?v=LyrqhruLhB') // return false
```

### isPositiveInteger
*Validate if the input is a positive Integer*
```jsx
  isPositiveInteger(12) // return true
  isPositiveInteger(-10) // return false
```

### isEven
*Validate if the input is a Even number*
```jsx
  isEven(12) // return true
  isEven(3) // return false
```

### isOdd
*Validate if the input is a odd number*
```jsx
  isOdd(3) // return true
  isOdd(10) // return false
```

### isMacAddress
*Validate if the input is a MAC Address*
```jsx
  isMacAddress('FF:FF:FF:FF:FF:FF') // return true
  isMacAddress('asman:asdas') // return false
```

### isleapYear
*Validate if the input is a leap year*
```jsx
  isleapYear(2020) // return true
  isleapYear(2017) // return false
```


### isIPaddress
*Validate if the input is a Ip address*
```jsx
  isIPaddress('192.168.0.1') // return true
  isIPaddress('192.168.0.') // return false
```

### factors
*returns factors of the given number*
```jsx
  factors(5) // return 0,1,5
```

### factorial
*returns factorial of the given number*
```jsx
  factorial(5) // return 120
```

### hasVowel
*Validate if the input has a vowel*
```jsx
  hasVowel('asskdsdf') // return true
  hasVowel('zxcvbn') // return false
```

### isPerfectSquare
*Validate if the input is a perfect square*
```jsx
  isPerfectSquare(9) // return true
  isPerfectSquare(6) // return false
```

### isBoolean
*Validate if the input is a boolean value*
```jsx
  isBoolean(true) // return true
  isBoolean(false) // return true
  isBoolean(1) // return false
```

### isRoman
*Validate if the input is Roman*
```jsx
  isRoman('IV') // return true
  isRoman('iv') // return true
  isRoman('ER') // return false
```

### isAge
*Validate if the input is a valid age*
```jsx
  isAge('23') // return true
  isAge(54) // return true
  isAge('567') // return false
  isAge(156) // return false
```
