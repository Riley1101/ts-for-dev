---
sidebar_position: 1
---

# Introduction

A programming language by microsoft that built entirely up on javascript.

It is a typed superset of javascript that compiles to plain javascript.

The main reason for using Typescript is to add static typing to Javascript.

## Why we need checking types?

For example,

```js
// Javascript
function add(a, b, c = 0) {
  return a + b + c;
}

// Typescript
function add(a: number, b: number): number {
  return a + b;
}
add(3, "4");
```

So by statically typing, we can avoid bugs that are caused by unexpectedly changing the type of a variable. We can always keep track of the type of variable which is a huge advantage while building complex applications.

In this series, I am gonna be talking about all the features of Typescript from the very basic to where you can use Typescript in all of your programs.

## Parts of Typescript

- Language
- Compiler
- Language server

## Some more reasons

### More clear code and great documentation

```ts
/**
 * Add two numbers
 * @param a first number
 * @param b second
 */
export async function addNumbers(a: number, b: number) {
  await timeout(500);
  return a + b;
}
```

### Better developer experience

![Auto Complete ](/img/auto-suggestion.png)

## Topics

```bash
Course topics
├──  Introduction to Typescript
   ├── Compiling ts program
   └── Variables and types
   └── Objects and arrays
   └── Interfaces and type-aliases
   └── Some exercises
   └── Functions
   └── Classes
   └── Generics
   └── Dictionaries and Map
   └── Scopes and Restraints
└── Challenges and projects
```

You will need to have an understanding in

- **Javascript**
- variables
- Arrays
- Objects
- Functions
- Arrow Functions
- Classes
- Destructuring
- javascript fundamentals

Overall a great understanding of Javascript.
