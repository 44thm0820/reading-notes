# Readings: Express REST API - class03 - 401

## Note from the student Rey Mercado to the grader


## Overview

Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

## Review, Research, and Discussion


## Preview

Skim the following materials in preparation for the upcoming lecture. Note the following as you browse the material, and be prepared to participate in discussions during lecture


## Reading

### ****[Review: ES6 Classes - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)****

Classes are special functions, and thus class syntax has two components: class expressions and class declarations. You declare a class using the class keyword with the name of the class. Class declarations unlike function declarations are not hoisted automatically. 

````JavaScript
class Rectangle {}
````

A class expression is the other way to define a class:

````JavaScript
// unnamed
let Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name);
// output: "Rectangle"

// named
let Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
console.log(Rectangle.name);
// output: "Rectangle2"

````
Class expressions are also not hoisted.
The body of a class is executed in strict mode.
The constructor method is a special method for creating and initializing an object created with a `class`.  There can only be one special method with the name `"constructor"` in a class. A constructor can use the `super` keyword to call the constructor of the super class. The `static` keyword defines a static method or property for a class which allows for variables and methods not to be made available to instances of the class.
Instance properties must be defined inside of class methods:

````JavaScript
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
````
Field declaration syntax is used with ES6 Classes:
````JavaScript
class Rectangle {
  height = 0;
  width;
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
````
Using the `extends` keyword allows the creation of a class that is a child of another class:
````JavaScript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name); // call the super class constructor and pass in the name parameter
  }

  speak() {
    console.log(`${this.name} barks.`);
  }
}

let d = new Dog('Mitzie');
d.speak(); // Mitzie barks.

````
If there is a constructor present in the subclass, the subclass (in the constructor) needs to first call super() before using "this".

The super keyword is used to call corresponding methods of super class. This is one advantage over prototype-based inheritance.

````JavaScript
class Cat {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

class Lion extends Cat {
  speak() {
    super.speak();
    console.log(`${this.name} roars.`);
  }
}

let l = new Lion('Fuzzy');
l.speak();
// Fuzzy makes a noise.
// Fuzzy roars.
````

Finally, a class can't be redefined.  Attempting to do so give back a `SyntaxError`.


### ****[Using Express Routing - expressjs.com](https://expressjs.com/en/guide/routing.html)****

this document from expressjs.com provides how someone could use the response object to send to client by using the many `methods` the response object has in Express to send data over the response object to the client:

**Response methods**

The methods on the response object (res) in the following table can send a response to the client, and terminate the request-response cycle. If none of these methods are called from a route handler, the client request will be left hanging.

| Method | Description |
| ----------- | ----------- |
|`res.download()` |	Prompt a file to be downloaded. |
|`res.end()` |	End the response process. |
|`res.json()` |	Send a JSON response. |
|`res.jsonp()` |	Send a JSON response with JSONP support. |
|`res.redirect()` |	Redirect a request. |
|`res.render()`	| Render a view template. |
|`res.send()`	| Send a response of various types. |
|`res.sendFile()` |	Send a file as an octet stream. |
|`res.sendStatus()` |	Set the response status code and send its string representation as the response body. |

Also you can make an `app.route()` to create chainable route handlers for a route path. <mark>Because the path is specified at a single location, creating modular routes is helpful, as is reducing redundancy and typos.</mark>
 See example below:
````JavaScript
app.route('/book')
  .get((req, res) => {
    res.send('Get a random book')
  })
  .post((req, res) => {
    res.send('Add a book')
  })
  .put((req, res) => {
    res.send('Update the book')
  })
````

`express.Router` is a class in Express that allows you to create modular, mountable route handlers. A `Router` instance is a complete middleware and routing system.
The following example creates a router as a module, loads a middleware function in it, defines some routes, and mounts the router module on a path in the main app.

Create a router file named birds.js in the app directory, with the following content:

````JavaScript
const express = require('express')
const router = express.Router()

// middleware that is specific to this router
router.use((req, res, next) => {
  console.log('Time: ', Date.now())
  next()
})
// define the home page route
router.get('/', (req, res) => {
  res.send('Birds home page')
})
// define the about route
router.get('/about', (req, res) => {
  res.send('About birds')
})

module.exports = router
````
Then load the router module in the app:

````JavaScript
const birds = require('./birds')

// ...

app.use('/birds', birds)
````
The app will now be able to handle requests to /birds and /birds/about, as well as call the timeLog middleware function that is specific to the route.

### ****[Express Routing - scotch.io/tutorials](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)****

Though tagged as a tutorial as out of date and no longer maintained in **digital ocean**, the article succeeds in explaining Express4.0 comes with the new `Router`, where `Router` is like a mini-Express application.

The article shows that regarding Express 4.0 Router, we can:

- `Use express.Router()` multiple times to define groups of routes
- Apply the `express.Router() `to a section of our site using `app.use()`
- Use route middleware to process requests
- Use route middleware to validate parameters using `.param()`
- Use `app.route()` as a shortcut to the Router to define multiple requests on a route
----

# Readings: Express REST API

Below you will find some reading material, code samples, and some additional resources that support today's topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

## Review, Research, and Discussion

In your reading notes page for this class, provide answers to the following prompts. Cite any external sources

1. Name 3 real world use cases where you'd want to change the request with custom middleware
1. True or false: The route handler is middleware?
1. In what ways can a middleware function end the process and send data to the browser?
1. At what point in the request lifecycle can you "inject" middleware?
1. What can cause express to error with "Request headers sent twice, cannot start a second response"

### Document the following Vocabulary Terms

| Term                            |
| ------------------------------- |
| Middleware                      |
| Request Object                  |
| Response Object                 |
| Application Middleware          |
| Routing Middleware              |
| Test Driven Development         |
| Behavioral Testing              |

## Preview

Skim the following materials in preparation for the upcoming lecture. Note the following as you browse the material, and be prepared to participate in discussions during lecture

1. Which 3 things had you heard about previously and now have better clarity on?
1. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
1. What are you most excited about trying to implement or see how it works?

### Preparation Materials

- [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes){:target="_blank"}
- [Using Express Routing](https://expressjs.com/en/guide/routing.html){:target="_blank"}
- [Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4){:target="_blank"}