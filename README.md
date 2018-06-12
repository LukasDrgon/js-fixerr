![Logo](js-fixerr.svg)[](https://www.npmjs.com/package/js-fixerr)
# js-fixerr  [![npm](logo.svg)](https://www.npmjs.com/package/js-fixerr) [![](https://data.jsdelivr.com/v1/package/npm/js-fixerr/badge)](https://www.jsdelivr.com/package/npm/js-fixerr)

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

you can also include it via CDN:
```html
<script src="https://cdn.jsdelivr.net/npm/js-fixerr/index.js"></script>
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
  try
  {
    fixerr.min('foobaar', 3) // return true
  }catch(e){
    console.log('Error in Input');
  }  

  try
  {
    fixerr.min('fooba12', 3) // return true
  }catch(e){
    console.log('Error in Input');
  }

  try
  {
    fixerr.min(34563, 4) // return true
  } catch(e){
    console.log('Error in Input'); 
  } 

  try
  {
    fixerr.min(345, 4) // return false  
  }catch(e){
    console.log('Error in Input'); 
  } 
  
  try
  {
    fixerr.min('foo', 5) // return false  
  }catch(e){
    console.log('Error in Input'); 
  }
  
```

### max
*Validate if the input is greater then the max value*
```jsx
  try
  {
    fixerr.max('foobaar', 6) // return true
  } catch(e){
    console.log('Error in Input');  
  }  

  try
  {
    fixerr.max(12345, 6) // return true
  } catch(e){
    console.log('Error in Input'); 
  }  

  try
  {
    fixerr.max(12345, 3) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  

  try
  {
    fixerr.max('foo', 2) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### length
*Validate if the string lie between the given value*
```jsx
  try
  {
    fixerr.length('foobaar', 0, 7) // return true
  } catch(e){
    console.log('Error in Input'); 
  }  

  try
  {
    fixerr.length(123456, 0, 7) // return true
  } catch(e){
    console.log('Error in Input'); 
  }  

  try
  {
    fixerr.length(123456567878, 0, 7) // return flase
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {  
    fixerr.length('foobaar', 0, 5); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### required
*Validate if the input is empty*
```jsx
  try
  {
    fixerr.required('foobaar') // return true
  } catch(e){
    console.log('Error in Input'); 
  } 
  
  try
  {
    fixerr.required(''); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {  
    fixerr.required(' '); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {  
    fixerr.required(); // return false
  } catch(e){
    console.log('Error in Input'); 
  }    
```

### noWhiteSpace
*Validate if the input has no whitespace*
```jsx
  try
  {
    ixerr.noWhiteSpace('foobaar') // return true
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {  
    fixerr.noWhiteSpace(' ') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {  
    fixerr.noWhiteSpace('') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
   
  try
  {  
    fixerr.noWhiteSpace('foo baar'); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### withWhiteSpace
*Validate if the input has whitespace*
```jsx
  try
  {
    fixerr.withWhiteSpace('foo baar') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
  
  try
  {  
    fixerr.withWhiteSpace('') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
  
  try
  {  
    fixerr.withWhiteSpace(' ') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
  
  try
  {  
    fixerr.withWhiteSpace('foobaar'); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### withSpecialChar
*Validate if the input has Special character*
```jsx
  try
  {
    fixerr.withSpecialChar('foo@$ba%ar') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
  
  try
  {  
    fixerr.withSpecialChar('f!oo~ar') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
  
  try
  { 
    fixerr.withSpecialChar(' ') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
  
  try
  {  
    fixerr.withSpecialChar('foobaar'); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### noSpecialChar
*Validate if the input has no Special character*
```jsx
  try
  {
    fixerr.noSpecialChar('foobaar') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
  

  try
  {
    fixerr.noSpecialChar('f!oo~ar') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
  

  try
  {
    fixerr.noSpecialChar('foo@ba^ar'); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### lower
*Validate if the input is in lower case*
```jsx
  try
  {
    fixerr.lower('foobaar') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.lower('fooBaar') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {
    fixerr.lower('Foobaar'); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### upper
*Validate if the input is in upper case*
```jsx
  try
  {
    fixerr.upper('FOOBAAR') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.upper('fooBaar') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.upper('Foobaar'); // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### string
*Validate if the input is a string*
```jsx
  try
  {
    fixerr.string('FOOBAAR') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.string('foobaar') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.string(1233) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### number
*Validate if the input is a number*
```jsx
  try
  {
    fixerr.number(12131) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.number('foobaar') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### noAlphaNumeric
*Validate if the input has no Alphanumeric characters*
```jsx
  try
  {
    fixerr.noAlphaNumeric('foobaar') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.noAlphaNumeric('fooba901') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### mobile
*Validate if the input is a 10 digit mobile number*
```jsx
  try
  {
    fixerr.mobile(1234567890) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.mobile(745387) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### email
*Validate if the input is a email address*
```jsx
  try
  {
    fixerr.email('jsfixerr@gmail.com') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.email('jsfixerr@com') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.email('jsfix err@ gmail com') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
    
```

### date
*Validate if the input is a date*
```jsx
  try
  {
    fixerr.date('10/12/2017') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.date('10-12-2017') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.date('16/34/3434') //return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### array
*Validate if the input is a array*
```jsx
  try
  {
    fixerr.array([23,23,90]) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.array('[12,23,546]') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.array(['a','b','c']) // return true
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isInteger
*Validate if the input is a Integer*
```jsx
  try
  {
    fixerr.isInteger(23) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isInteger('12') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isInteger('a') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isFloat
*Validate if the input is a Float*
```jsx
  try
  {
    fixerr.isFloat(23.12) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isFloat('12') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isFloat(34) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```
### vowel
*Validate if the input is a vowel*
```jsx
  try
  {
    fixerr.vowel('a') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.vowel('aeo') // return true
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {
    fixerr.vowel('aeoiu') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.vowel('sdf') // return false
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.vowel('sdfa') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isPrime
*Validate if the input is a prime number*
```jsx
  try
  {
    fixerr.isPrime(7) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isPrime(12) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isVideoUrl
*Validate if the input is a youtube video Url*
```jsx
  try
  {
    fixerr.isVideoUrl('https://www.youtube.com/watch?v=LyrqhruLhBA') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isVideoUrl('https://www.youtube.com/watch?v=LyrqhruLhB') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isPositiveInteger
*Validate if the input is a positive Integer*
```jsx
  try
  {
    fixerr.isPositiveInteger(12) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isPositiveInteger(-10) // return false
  } catch(e){
    console.log('Error in Input'); 
  }
```

### isEven
*Validate if the input is a Even number*
```jsx
  try
  {
    fixerr.isEven(12) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isEven(3) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isOdd
*Validate if the input is a odd number*
```jsx
  try
  {
    fixerr.isOdd(3) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isOdd(10) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isMacAddress
*Validate if the input is a MAC Address*
```jsx
  try
  {
    fixerr.isMacAddress('FF:FF:FF:FF:FF:FF') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isMacAddress('asman:asdas') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isleapYear
*Validate if the input is a leap year*
```jsx
  try
  {
    fixerr.isleapYear(2020) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isleapYear(2017) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```


### isIPaddress
*Validate if the input is a Ip address*
```jsx
  try
  {
    fixerr.isIPaddress('192.168.0.1') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isIPaddress('192.168.0.') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### factors
*returns factors of the given number*
```jsx
  try
  {
    fixerr.factors(5) // return 0,1,5
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### factorial
*returns factorial of the given number*
```jsx
  try
  {
    fixerr.factorial(5) // return 120
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### hasVowel
*Validate if the input has a vowel*
```jsx
  try
  {
    fixerr.hasVowel('asskdsdf') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.hasVowel('zxcvbn') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isPerfectSquare
*Validate if the input is a perfect square*
```jsx
  try
  {
    fixerr.isPerfectSquare(9) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isPerfectSquare(6) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isBoolean
*Validate if the input is a boolean value*
```jsx
  try
  {
    fixerr.isBoolean(true) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isBoolean(false) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
    
  try
  {
    fixerr.isBoolean(1) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isRoman
*Validate if the input is Roman*
```jsx
  try
  {
    fixerr.isRoman('IV') // return true
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {
    fixerr.isRoman('iv') // return true
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {
    fixerr.isRoman('ER') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```

### isAge
*Validate if the input is a valid age*
```jsx
  try
  {
    fixerr.isAge('23') // return true
  } catch(e){
    console.log('Error in Input'); 
  }
  
  try
  {
    fixerr.isAge(54) // return true
  } catch(e){
    console.log('Error in Input'); 
  }
  
  try
  {
    fixerr.isAge('567') // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
  
  try
  {
    fixerr.isAge(156) // return false
  } catch(e){
    console.log('Error in Input'); 
  }  
```
