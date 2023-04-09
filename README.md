# es6Features
ECMAScript 6

## Introduction
ECMAScript 2015 is also known as ES6 and ECMAScript 6. ES6 has many new features that can help a developer understand and write code more efficiently.

ES6 is a feature-rich advancement to ES5, the previous version of JavaScript, and is 100% backwards compatible. One can write code in ES5 and gradually switch to ES6 features with ease.

See the [ES6 standard](http://www.ecma-international.org/ecma-262/6.0/) for full specification of the ECMAScript 6 language.

Below is the list of ES6 features every JS developer should know,
- [let + const](#let--const)
- [arrow](#arrow)
- [spread and rest(...)](#spread--rest)
- [for..of](#forof-loop)
- [default parameters](#default-parameters)
- [template strings](#template-strings)

## ECMAScript 6 Features

### let + const

The `let` keyword allows you to declare a variable with block scope.

```Javascript
var x = 10;
console.log(x); //x is 10
{
    let x = 20;
    console.log(x); //x is 20
}
console.log(x); //x is 10
```

The `const` keyword allows you to declare a constant (a JavaScript variable with a constant value).
Constants are similar to let variables, except that the value cannot be changed.

```Javascript
var x = 10;
console.log(x); //x is 10
{
    const x = 20;
    console.log(x); //x is 20
    x = 30; //TypeError: Assignment to constant variable.
}
console.log(x); //x is 10
```
### Arrow
Arrow functions(also known as ‘fat arrow functions’). Arrow functions allows a short syntax for writing function expressions.
You don't need the `function` keyword, the `return` keyword, and the **curly brackets**.

``` Javascript
// ES5
var x = function(x, y) {
   return x * y;
}

console.log(x(2,2)); // return 4

// ES6
let a = (a, b) => a * b;
console.log(a(2,2)); //return 4
```

### Spread + Rest
Rest and spread syntax use … (three dots) notation.
Spread syntax expands an array into separate elements, while a rest syntax condenses array elements into a single element.

``` Javascript
//Example Spread
const a = [1, 2, 3, 4, 5];
const b = [6, 7, 8, 9, 10];

const c = [ ...a, ...b ];
console.log(c); //merge both a and c

//Example Rest
const numbers = [10,30,20,50,60];
let maxValue = Math.max(...numbers);
console.log(maxValue); //return 60
```

### for..of loop
The JS `for/of` statement loops through the values of an iterable such as Arrays, Strings, Maps, NodeLists and more.

``` JavaScript
const message = ["Hello", "Good", "Morning!"];
let text = "";

for (let x of message) {
  text += x + " ";
}

console.log(text); //print Hello Good Morning!
```

### Default Parameters
ES6 allows function parameters to have default values.

``` JavaScript
function add(x, y = 20) {
  // y is 20 if not passed or undefined
  return x + y;
}
console.log(add(5)); // will return 25
```

### Template Strings
In ES6, we can use a new syntax ${PARAMETER} inside of the back-ticked.

``` JavaScript
//Single Line
`In JavaScript '\n' is a line-feed.`

//Multi Line
`Johny Johny Yes Papa,     
Eating sugar?  No, papa!
Telling lies? No, papa!
Open your mouth Ah, ah, ah!`

let name = 'Charlie';
`Hello, I am ${name}`
```

