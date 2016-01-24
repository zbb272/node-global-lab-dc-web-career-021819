# Use REPL and Global

## Objectives

1. Use REPL
1. Access global
1. Understand scoping and explicit vs. implicit declaration

## Introduction

Understanding global and scoping will give you a good foundation for future development.

## Instructions

1. Enter Node REPL
1. Print global object
1. Narrow down to specific info of process (`global.process`)
1. Create a global variable `user` explicitly with `global.user = {admin: false}`
2. Create a global variable implicitly with `var account = {balance: 1000}` 
3. Open a new REPL and check for values of user and account (ReferenceError)
2. Go back to the 1st REPL and print user and account with `global.user` and `global.account`
3. Delete `user` with `delete user` (true) and print it again (ReferenceError)
4. Delete `account` with `delete account` (false) and print it again ({balance: 1000})
3. Exit REPL
4. Contemplate on the fact that user and account reacted differently to the `delete` operator. 


### Extra Info

To understand the discrepancy, you need to know how `delete` works and what was the difference between `user` and `account` in the ways they were created (explicit with `global` vs. implicit with `var` ).

* [Delete operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete)

