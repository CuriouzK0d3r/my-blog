---
author: "Alexandros"
title: "Learn You a Functional Programming for Great Good!"
date: 2021-07-08T00:00:00.000Z
tags: ["Haskell", "Functional Programming"]
categories: ["Programming"]
description: "Why should we learn FP?"

featuredImage: "/images/fp.webp"
featuredImagePreview: "/images/fp.webp"

hiddenFromHomePage: false
hiddenFromSearch: false

lightgallery: true
---

Level of knowledge required: This article requires some programming background to be fully understood.

## Introduction

I am sure you have noticed the silly syntax in this article's title. It is inspired by a popular introductory book for the Haskell language, called “Learn You a Haskell for Great Good!” [1].
Which could probably be perceived as “Learn Haskell for great benefit”. Haskell is one of the so-called purely functional programming languages. Or more precisely, almost purely functional.

But is there a benefit in learning Haskell or - even more - functional programming?
Absolutely. I strongly believe that learning Functional Programming can make you a better developer.

## Starting with some basics

### Definitions

Functional programming is a **declarative** paradigm of building software by composing **pure functions**, avoiding **shared state**, **mutable data** and **side-effects**.

In short, functional programming is a catch-all term for a way of writing code that is focused on composing pure functions, actually using the innovations in type systems made in the last few decades, and overall being awesome [2].

Functional languages emphasize expressions and declarations rather than the execution of statements. Therefore, unlike other procedures which depend on a local or global state, value output in FP depends only on the arguments passed to the function.

### Pure Functions

A pure function [3] is a function which:

- Given the same input, always return the same output.
- Has no side-effects (immutable)

![purefunctionrule.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1624823110043/i7F3itaco.jpeg)

Unfortunately, understanding FP in depth requires knowledge of math and computability theory. In the core of functional programming lies the lambda calculus. The first and purest functional programming language.

For a fun introduction to Computability, watch this [YouTube clip](https://www.youtube.com/watch?v=GnpcMCW0RUA) by the great Philip Wadler! About lambda calculus, there are numerous online [resources](https://www.inf.fu-berlin.de/lehre/WS03/alpi/lambda.pdf).

Now let’s move to more practical aspects!

## Pure and not so pure functional languages

Let’s be clear. All languages have side effects. Even Haskell, which is considered the purest of the modern languages. Side-effects are necessary to interact with the filesystem and other parts of the OS.
However, the way these effects are handled and structured can help us decide about the purity of the language. For example, Haskell has a unique way of handling side-effects, with an abstraction called Monad. Wondering what Monad (or a monoid) is? Hmm, maybe we will discuss this in a future post.

Furthermore, some languages adopt functional features (like Java with lambdas) but are still mainly focused on a procedural/OOP programming style.
While in others, pure functions are the main building block of the code. See Clojure, Scala, Elixir.

## What languages shall I try?

Well, it wildly depends on your domain of interest! For front-end web development, **Elm**, **Elixir**, **ReasonML**, **PureScript**, and maybe **ClojureScript** are great options!

For backend, I would strongly suggest checking **Elixir**, **F#**, and **Racket**. **Rust** and **Haskell** are also options, although I generally had issues with the related Haskell modules I had tried in the past.

For native mobile app development, I suggest **Kotlin** and **Swift**, for Android and iOS respectively.

For lower-level programming like systems programming, **Rust** is a no-brainer.

For concurrency and distributed systems, I suggest **Elixir**, **Scala**, and **Erlang**.

For language writers, **Haskell**, **Rust** and **OCaml**.

## Benefits of FP languages

To be honest, I am not an expert in functional programming. However, experts suggest that pure functions are easier to test, lead to fewer bugs, and tend to have their state isolated, making it easier to comprehend. FP code is also more predictable.

I will add that FP is great for concurrency. The lack of side effects and immutability guarantees deterministic execution. Distributed algorithms also heavily benefit from this architecture.

In my opinion, functional code is also more elegant. Observe the following functional and imperative code examples in JavaScript:

Imperative style:

`const salaries = [10000, 20000, 30000, 40000];`  
`let totalSalary = 0;`  
`for (let I = 0; I < salaries.length; I++) {`  
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; `totalSalary += salaries[I]`  
`}`

Functional style:

`const salaries = [10000, 20000, 30000, 40000];`  
`const totalSalary = salaries.reduce((acc, value) => acc + value, 0);`

Isn’t it more elegant?

## How is this going to help me?

What if you are using a language we haven’t mentioned so far? Like C# or Java? Is learning Haskell or Clojure going to help you? Of course.

Every experienced developer knows that programming is much more than the language syntax and the frameworks you are using. The difference is being made in the way you are approaching problems.

However, working in a programming language affects how you think about problems. If your language gives you some features, you think in terms of those features. Learning new programming languages gives you a different feature set, and this suggests other ways to address a problem.

Functional programming is closer to mathematical thinking, which a more natural way of thought for humans [4]. It makes the process of designing your system and code more effective.
Practicing FP forces you to lean towards this style of thinking.
And eventually makes you a better developer.

## Conclusion

So this is it! This article intended to provide a few arguments in favor of Functional Programming. I hope it achieved this goal.

I strongly recommend giving it a try. If you don’t know where to start, pick Haskell. It will be an immersive experience in the world of pure functions.
I cannot think of a better introduction to the magical space of mathematics, functional programming, and the theory of programming languages.

Start with **Learn You a Haskell for Great Good!** or [Real World Haskell](http://book.realworldhaskell.org/) and you won’t regret it.

## References

1. [Learn You a Haskell for Great Good!](http://learnyouahaskell.com/)
2. [What Is Functional Programming?](https://serokell.io/blog/introduction-to-functional-programming)
3. [Functional (Programming) mindset](https://www.codingame.com/playgrounds/24002/functional-programming-mindset/functional-programming-definition-)
4. [Think in Math](https://justinmeiners.github.io/think-in-math)