### Function
### 'this' in Function
### Arrow Function
### 'this' in Arrow Function
### Arrow Function
### Anonymous Function

-----------------------------

### Function

* In Javascript We can use function as:
  * As a nomal function
  * As a Class, Each function will return a new object
  
```js
// As a class
function Person(){
  this.name = "tuan" 
  console.log("the name is : " + this.name) // the name is : tuan
}

var p = new Person() // the name is : tuan

console.log("My name :" + p.name) // My name :tuan

```

### 'this' in Function

* **'this'** in function is the object that called the function

```js
function Person(){
  console.log("the name is : " + this.name)  // this = p
}

var p = new Person()
```


* By default:
```js
// If the function is not called by any object it is default called by global context

function Person(){
  console.log("the name is : " + this.name)  // this = global context
}

Person() // Call Person method by global context
```

* Example 1

```js
// 'this' is the context (object) that called the Person function
// in this case 'this' is a global context => 'this' is global context, because Person called by global context

var name = "tuan"

function Person(){
  console.log("the name is : " + this.name) // the name is : tuan
}

Person() // the name is : tuan , because in this case 'this' = global context => this.name = tuan

var p = new Person() // the name is : undefined , because is this case 'this' = object p => this.name is p.name => undefined
```

* Example 2

```js
// this.name is undefined because 'this' is global context and we have no variable name in global context

function Person(){
  var name = "tuan" 
  console.log("the name is : " + this.name) // the name is : undefined
}

Person() // the name is : undefined

var p = new Person() // the name is : undefined
```

* Example 3

```js
// Before call Person method global context have no variable 'name'
// After call Person method the global context have : name = "tuan"

function Person(){
  this.name = "tuan" 
  console.log("the name is : " + this.name) 
}

console.log("the name is : " + this.name) //the name is : undefined

Person() // the name is : tuan

console.log("the name is : " + this.name) //the name is : tuan
```

* Example 4 

```js
// Before call Person method global context have no variable 'name'
// After call Person method the p object have : p.name = "tuan"

function Person(){
  this.name = "tuan" 
  console.log("the name is : " + this.name) 
}

console.log("the name is : " + this.name) //the name is : undefined

var p = new Person() // the name is : tuan

console.log("the name is : " + p.name) //the name is : tuan

console.log("the name is : " + this.name) //the name is : undefined
```

### Arrow Function

* Arrow functions were introduced in ES6.
* Arrow functions allow us to write shorter function syntax:

```js
hello = () => {
  return "Hello World!";
}
```

* If the function has only one statement, and the statement returns a value, you can remove the brackets and the return keyword:

```js
hello = () => "Hello World!";
```

* Arrow Function have only 1 Parameters:

```js
hello = (val) => "Hello " + val;

OR

hello = val => "Hello " + val;
```

### 'this' in Arrow Function

* **this** is also different in **arrow functions** compared to **regular functions**.
* In short, with **arrow functions there are no binding of this**.

* **In regular functions** : `this` keyword represented the object that called the function
* **In arrow functions the** : `this` keyword always represents the object that defined the arrow function.



### Anonymous Function

* An anonymous function is a function that was declared without any named identifier to refer to it. 
* As such, an anonymous function is usually not accessible after its initial creation.

* Anonymous function definition:

```js
var hello = function() {
  alert('I am anonymous');
}
hello();
```




