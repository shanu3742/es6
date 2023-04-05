# es6


- let and const 
- multi-line String
- Template Literals
- Default parameter(function)
- Arrow function
- rest and spread 
- Destracturing
- callback function
- class

>**callback**
**if we pass a function as argument to another function it's called as callback function**
*example-1*
```javascript
function positiveNumber(x) {
return x>0?true:false
}
function  absArray(array,callback) {
  let positive=[]
  for(let i=0;i<array.length;i++){
    if(callback(array[i])){
      positive.push(array[i])
}
}
  return positive
}

console.log(absArray([2,-1,7,-3],positiveNumber))
/**here positiveNumber function is passed as argument to absArray function
*and the role is positiveNumber function is return true or false,
*if a number is positive it return true else false
**/

/**if you don't know about function argument if you pass some value on function call that value call as function argument
*sum(3,4)//here 3,4 is function argument
* function argument may be number,string,boolean,null,undefined ,variable function ,object,array, it's depends on requirement
**/
```
> **another way to do same**

```javascript
function  absArray(array,callback) {
  let positive=[]
  for(let i=0;i<array.length;i++){
    if(callback(array[i])){
      positive.push(array[i])
}
}
  return positive
}

console.log(absArray([2,-1,7,-3],(x) => x>0?true:false))

/**
*here we directly pass function in argument ,you can create function in argument ,
*however it's better to avoid it but if your function is to small then you can do it ,like how i did above 
*i just created an anyynomus function and perform my require operation and return  true or false based on condition
*it's smae as map ,filter and other array method 
**/
```

>**array method**
- map
- filter
- reduce
- for of
- for in


- JavaScript Object Entries
 > **ECMAScript 2017 added the Object.entries() method to objects.Object.entries() returns an array of the key/value pairs in an object:**
```javascript
const person = {
  firstName : "John",
  lastName : "Doe",
  age : 50,
  eyeColor : "blue"
};

let text = Object.entries(person);
```



- JavaScript Object Values
> **Object.values() are similar to Object.entries(), but returns a single dimension array of the object values:**

```javascript
const person = {
  firstName : "John",
  lastName : "Doe",
  age : 50,
  eyeColor : "blue"
};

let text = Object.values(person);
```


- JavaScript Object keys
> **Object.values() are similar to Object.entries(), but returns a single dimension array of the object values:**

```javascript
const person = {
  firstName : "John",
  lastName : "Doe",
  age : 50,
  eyeColor : "blue"
};

let text = Object.keys(person);

```

- JavaScript Array flat()
```javascript
const myArr = [[1,2],[3,4],[5,6]];
const newArr = myArr.flat();

```

- JavaScript Object fromEntries()
```javascript
const fruits = [
["apples", 300],
["pears", 900],
["bananas", 500]
];

const myObj = Object.fromEntries(fruits);
````
## ES6 new feature

> JavaScript Numeric Separator (_)
```javascript
const num1 = 1_000_000_000;
const num2 = 1000000000;
(num1 === num2);
```

> BigInt-
- one type
```javascript
let x = 9999999999999999;
let y = 9999999999999999n;
```
- second type-
```javascript
let x = 1234567890123456789012345n;
let y = BigInt(1234567890123456789012345)
```

> **The Nullish Coalescing Operator (??) The ?? operator returns the first argument if it is not nullish (null or undefined).Otherwise it returns the second.**
```javascript
let name = null;
let text = "missing";
let result = name ?? text;
```

> **The Optional Chaining Operator (?.)The Optional Chaining Operator returns undefined if an object is undefined or null (instead of throwing an error).**

*exaple-*
```javascript
const car = {type:"Fiat", model:"500", color:"white"};
let name = car?.name;
```


>**The &&= Operator(The Logical AND Assignment Operator is used between two values.If the first value is true, the second value is assigned.)**
*exaple-*
```javascript
let x = 10;
x &&= 5;
```


>**The ||= Operator (The Logical OR Assignment Operator is used between two values.If the first value is false, the second value is assigned.)**

*example-*
```javascript
let x = 10;
x ||= 5;
```

>**??= (Nullish Coalescing Assignment Operator)-The Nullish Coalescing Assignment Operator is used between two values.If the first value is undefined or null, the second value is assigned.**
*exapmle-*
```javascript
let x = 10;
x ??= 5;
```

## Math method
- >**Math.round(x)**	Returns x rounded to its nearest integer

- >**Math.ceil(x)**	Returns x rounded up to its nearest integer

- >**Math.floor(x)**	Returns x rounded down to its nearest integer

- >**Math.trunc(x)**	Returns the integer part of x (new in ES6)

- >**Math.pow(x, y)** returns the value of x to the power of y:

- >**Math.sqrt(x)** returns the square root of x:

- >**Math.abs(x)** returns the absolute (positive) value of x:

- >**Math.min()** and Math.max() can be used to find the lowest or highest value in a list of arguments:

- >**Math.random()** returns a random number between 0 (inclusive), and 1 (exclusive):

- >**Math.log(x)** returns the natural logarithm of x.

### not regulary used math method


- abs(x)	Returns the absolute value of x

- acos(x)	Returns the arccosine of x, in radians

- acosh(x)	Returns the hyperbolic arccosine of x

- asin(x)	Returns the arcsine of x, in radians

- asinh(x)	Returns the hyperbolic arcsine of x

- atan(x)	Returns the arctangent of x as a numeric value between -PI/2 and PI/2 radians

- atan2(y, x)	Returns the arctangent of the quotient of its arguments

- atanh(x)	Returns the hyperbolic arctangent of x

- cbrt(x)	Returns the cubic root of x

- ceil(x)	Returns x, rounded upwards to the nearest integer

- cos(x)	Returns the cosine of x (x is in radians)

- cosh(x)	Returns the hyperbolic cosine of x

- exp(x)	Returns the value of Ex

- floor(x)	Returns x, rounded downwards to the nearest integer

- log(x)	Returns the natural logarithm (base E) of x

- max(x, y, z, ..., n)	Returns the number with the highest value

- min(x, y, z, ..., n)	Returns the number with the lowest value

- pow(x, y)	Returns the value of x to the power of y

- random()	Returns a random number between 0 and 1

- round(x)	Rounds x to the nearest integer

- sign(x)	Returns if x is negative, null or positive (-1, 0, 1)

- sin(x)	Returns the sine of x (x is in radians)

- sinh(x)	Returns the hyperbolic sine of x

- sqrt(x)	Returns the square root of x

- tan(x)	Returns the tangent of an angle

- tanh(x)	Returns the hyperbolic tangent of a number

- trunc(x)	Returns the integer part of a number (x)


## Date and Time


- url
> https://docs.google.com/presentation/d/1bTXtmd1JDaPTwOVWYti78a7J7wH_TkB8/edit?usp=drivesdk&ouid=111425862082846915926&rtpof=true&sd=true



## last but not least 
- >async function(promises)
- >setTmeOut
- >setTimeInterval

