# Use REPL and Global

## Objectives

1. Use REPL
2. Access global
3. Use explicit vs. implicit declarations

## Introduction

Scoping is about defining and accessing variables/objects/functions. Here's a small example which can illustrate how dangerous it can be to not understand scope: our program uses a variable named `list` and module A uses a variable named `list`. When we import module A, the original `list` of the program is lost!

Understanding global and scoping will give you a good foundation for future development.

In this lab, we're going to be using the Node REPL to create several bank accounts and users in different scopes.

## Instructions

1. Enter Node REPL
1. Print the `global` object
1. Print the `process` object (`global.process`)
1. Create a global variable `user` explicitly with `global.user = {admin: false}`
1. Create a global variable implicitly with `var account = {balance: 1000}`
1. Open a new REPL and check for values of user and account (ReferenceError means the variable is undefined)
1. Go back to the first REPL and print user and account with `global.user` and `global.account`
1. Delete `user` with `delete user` (true) and print it again. You should get `ReferenceError` because you deleted `user`.
1. Delete `account` with `delete account` (false) and print it again ({balance: 1000})
1. Exit REPL
1. Contemplate on the fact that user and account reacted differently to the `delete` operator. Read the extra info if you forgot how `delete` works (it's JavaScript and not exclusive to Node).


### Extra Info

To understand the discrepancy, you need to know how `delete` works and what was the difference between `user` and `account` in the ways they were created (explicit with `global` vs. implicit with `var` ).

* [Delete operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete)

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/node-global-lab' title='node-global-lab'>node-global-lab</a> on Learn.co and start learning to code for free.</p>

<p class='util--hide'>View <a href='https://learn.co/lessons/node-global-lab'>Node Global Lab</a> on Learn.co and start learning to code for free.</p>

//done
