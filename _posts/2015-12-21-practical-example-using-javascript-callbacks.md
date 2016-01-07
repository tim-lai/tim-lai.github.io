---
layout: post
title: Practical Example for Using Javascript Callbacks
---
Node.js is the standard when it comes to building your own web application server. It is lightweight and its capabilities are extended its huge npm package ecosystem. 

Express is a middleware framework for Node.js, and it lets you chain as many function calls as needed. Order does matter, and you can proceed to the next function using next(). Express also can be extended with Promises, e.g. Bluebird, which allows for chaining of asynchronous events. 

Callbacks allow the chaining of asynchronous functions. There is no break within the function until the actions preceding the callback are completed. In the meantime, other processes outside of the function can continue to execute. Other processes in the logic chain should not have dependencies on the function if they are not linked through callbacks.

Taking advantage of callbacks is another good reason to use modularity in your code. Considering the widespread use of Node.js in web applications, javascript callbacks are critically important for every javascript programmer to use and understand.
