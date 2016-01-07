---
layout: post
title: Intro to Functional Programming in Javascript
---
Javascript offers  many benefits to its developer. It is powerful, it is fast, and it is flexible. One of the reasons for Javascript's power is the concept of functional programming.  

Functional programming uses higher-order functions that takes a function and a list as its arguments, then applies the given function and list in order to return a result. Functional programs avoids side effects and provides referential transparency. This allows for easier testing, verification, and optimization of programs. 

An analogy to functional programming is principles of good management. A good manager is primarily concerned about obtaining correct results, and is less interested in the details of how the result is obtained. The less time a good manager spends doing the work of their subordinates, the more tasks they can oversee and get done. 

Ideally, each team member task is also well defined and scoped such that their work can be done independent of other team members. The work of each team member can be verified on a task by task basis.  Also, team members work faster and with less overhead because they are allowed to choose how to complete their task rather than constantly checking for approvals. 

Similarly in functional programs, the manager, known as a first-class function, delegates tasks to other functions who perform their task then return their results to the original function. 

The first-class function may call on many helper functions, just like a manager who is responsible for many team members. However, each task is independent from each other and will not interfere or collide with each other in memory.  Each task also can be independently optimized and verified for its performance.

