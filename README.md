# Use REPL and Global

## Objectives

1. Use REPL
2. Access global
3. Understand scoping and explicit vs. implicit declaration

## Introduction

Understanding global and scoping will give you a good foundation for future development.

## Instructions

1. Enter Node REPL
1. Print the `global` object
1. Print the `process` object (`global.process`)
1. Create a global variable `user` explicitly with `global.user = {admin: false}`
1. Create a global variable implicitly with `var account = {balance: 1000}`
1. Open a new REPL and check for values of user and account (ReferenceError)
1. Go back to the 1st REPL and print user and account with `global.user` and `global.account`
1. Delete `user` with `delete user` (true) and print it again. You should get `ReferenceError` because you deleted `user`.
1. Delete `account` with `delete account` (false) and print it again ({balance: 1000})
1. Exit REPL
1. Contemplate on the fact that user and account reacted differently to the `delete` operator. Read the extra info if you forgot how `delete` works (it's JavaScript, not exclusive to Node).


### Extra Info

To understand the discrepancy, you need to know how `delete` works and what was the difference between `user` and `account` in the ways they were created (explicit with `global` vs. implicit with `var` ).

* [Delete operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete)

## Solution

`user` was created explicitly and `account` implicitly. The way `delete` works, it removes the property of an object and returns true of false. It has no effect on variable or function names.

When we delete `user` it is a real property of `global` and thus we get true. On the other hand, when we delete `accounts`, it's a non-configurable property of `global` due to `var`, so `delete` fails.