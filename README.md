# **FizzBuzz Challenge**
-------

FizzBuzz Site: https://camronldnf.github.io/fizz_buzz_js/

Repo: https://github.com/CamronLDNF/fizz_buzz_js

## **Overview**
This challenge was to recreate the FizzBuzz challenge in Javascript.


## **Questions**

### Question 1:

#### In your README to the best of your knowledge please explain what the following lines of code do?

    let  fizzBuzz = fs.readFileSync('./src/js/fizz-buzz.js');
    eval( fizzBuzz + `\nexports.FizzBuzz = FizzBuzz;`)

#### Answer:

* The Node.js File System (fs) module allows you to work with the file system on your computer.
* The Node fs module provides an API for interacting with the file system. To use the module, first use the `require('fs')` method to invoke the fs module, like this:

    `const fs = require('fs');`

Common use for the File System (fs) module:

Read files
Create files
Update files
Delete files
Rename files

As far as reading files go, there are two ways one can open and read files using the fs module:

**fs.readFile** is the most common method  and runs asynchronously. This one should be used whenever possible to avoid blocking the main execution thread. 

**fs.readFileSync** method however runs synchronously (blocking). In other words, the file contents are returned directly from the function call and the execution thread is blocked while it loads the file. Best practice is to use this in start-up sections of the program (like when we're loading config files) or in command-line apps where blocking the main thread isn't a big deal.

`let fizzBuzz` simply declares a variable and assigns it to the content returned from that file.

The `eval()` function evaluates any string passed in to it as JavaScript code. The string can represent a JavaScript expression, statement, or sequence of statements. 

The `\n` is simply JS code for creating a new line.

`exports` is an object (module.exports). So, you can attach properties or methods to it. In `exports.FizzBuzz = FizzBuzz;` we have attached a property "FizzBuzz" with the value `FizzBuzz` to the exports object. Now, you can import and use this module in _other_ files as shown below.
```
#app.js
var anyName = require('./sourceFileName.js');

console.log(anyName.FizzBuzz);
```

Read more [here](http://www.tutorialsteacher.com/nodejs/nodejs-module-exports)

### Question 2:

#### In your README to the best of your knowledge please explain why we are placing the code outside the it block?

    let fizzBuzz = new FizzBuzz


#### Answer:

* To create a new instance of the FizzBuzz class for the tests.


### Question 3:

#### In your README to the best of your knowledge please explain the difference between using === and == in JS?

#### Answer:

* ‘===‘ means the the values have to match in both data type and value
* ‘==‘ means it can just match in value (so for example ’123’ == 123 would evaluate to true)


### Question 4:

#### In your README to the best of your knowledge please explain why we are moving (number % 5 === 0) to the top?

#### Answer:

* Because the code is read top-down, so it wouldn't evaluate for 5 otherwise if it renders something as true before it gets to 5. 


### Question 5:

#### In your README to the best of your knowledge please explain the difference between feature and unit test?

#### Answer:

* Unit Tests are written from a programmers perspective. They are made to ensure that a particular method (or a unit) of a class performs a set of specific tasks.

* Feature Tests are written from the user's perspective. They ensure that the system is functioning as users are expecting it to.


### Question 6:

####  In your README to the best of your knowledge please explain what expectations are in the context of testing are?

#### Answer:

* It’s the assertion, i.e., what you expect the source code to return for that given function / feature that is being tested.


### Question 7:

####  In your README to the best of your knowledge please write a line to line explanation of what is happening in this code?

#### Answer:

* First, the fizz-buzz.js source code is being linked to the index file. Then, the DOM is connected to the index file and event listeners and event handlers are embedded. 


### Question 8:

#### In your README to the best of your knowledge please explain what a CDN (Content Delivery Network) is?

#### Answer:

* A content delivery network is a distributed platform of servers optimized to deliver content including web applications and streaming media. This network of servers is dispersed across many physical and network locations, in order to respond directly to end user requests for web content and fast, secure media delivery. It acts as an intermediary between a content server, also known as the origin, and its end users or clients.
