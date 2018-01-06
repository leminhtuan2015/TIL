### JavaScript Class

-----------------------------------------------------
### JavaScript Class

* **Classes** in Javascript are **"special functions"**

```js
class Foo {}

console.log(typeof Foo); // function
```

#### Ways to create class

* **Javascript Class declarations (ECMAScript 2015)**

```js
class Person {
  constructor(name, age) {
    this.name = name; // this = person : this is a object is call the Person function
    this.age = age;
  }
}

var person = new Person("tuan", 1)
```
* **Javascript Class expressions (ECMAScript 2015)**

```js
// unnamed
var Person = class {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};

// named
var Person = class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
};
```


* **Javascript Class (from function)**
```js
function Person(name) {
  this.name = name
  this.showName = function(){
      console.log("My name is : " + name)
  }
}

var person = new Person("tuan") // Create new Persion object

// Use properties and methods of object

person.name // 'tuan'
person.showName()  // My name is : tuan
```

* **Javascript Class in Nodejs**

```js
function Person(name) {
  this.name = name
  this.showName = function(){
      console.log("My name is : " + name)
  }
}

module.exports = Person
```

```js
// constructor call
var Person = require("../models/Person")
var tuan = new Person('Tuan');

tuan.showName()
```








