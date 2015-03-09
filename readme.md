# Functional Programming Jargons

> The whole idea of this repos is to try and define jargons from combinatorics and category theory jargons that are used in functional programming in a easier fashion.

__Let's try and define these with examples, this is a WIP please feel free to send PR ;)__


## Arity

> The number of arguments a function takes.

```js
const sum = (a, b) => a + b;

const arity = sum.length;
console.log(arity);
// => 2
// The arity of sum is 2
```
---

## Higher Order Functions (HOF)
> A function for which both the input and the output are functions.

```js
let greet = (name) => () => `Hello ${name}!`;
```

```js
greet("HOF")(); // Hello HOF!
```

## Partial Application
> The process of getting a function with lesser arity compared to the original
function by fixing the number of arguments is known as partial application.

```js
let sum = (a, b) => a + b;

// partially applying `a` to `40`
let partial = sum.bind(null, 40);

// Invoking it with `b`
partial(2); //=> 42
```

---

## Currying
> The process of converting a function with multiple arity into the same function with less arity.

```js
let sum = (a,b) => a+b;

let curriedSum = function(a) {
    return function(b) {
        return a + b;
    };
};

curriedSum(40)(2) // 42.
```

---

## Purity

---

## Side effects

---

## Idempotency

---

## Contracts

---

## Guarded Functions

---

## Categories

---

## Functor
> Structure that can be mapped over.

Simplest functor in javascript is an `Array`

```js
[2,3,4].map( function(n) {
  return n + 2;
}); // [4,6,8]
```
---

## Referential Transparency

> An expression that can be replaced with its value without changing the
behaviour of the program is said to be referential transparent.

Say we have function greet:

```js
let greet = () => "Hello World!";
```

Any invocation of `greet()` can be replaced with `Hello World!` hence greet is
referential transparent.

---

## Monoid

---

## Monad

---

##Comonad
---

## Applicative Functor

---


## Morphism

---

## Setoid

---

## Semigroup

---

## Chain
---


