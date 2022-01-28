---
author: Alexandros
title: This is a JavaScript world! 5 Languages that compile to JS
date: 2022-01-26T00:00:00.000+00:00
tags:
- JavaScript
- CoffeeScript
- ReScript
categories:
- Programming
description: 5 Languages that compile to JS
featuredImage: "/images/transpilation_diagram.jpg"
featuredImagePreview: ''
hiddenFromHomePage: false
hiddenFromSearch: false
lightgallery: true

---
If you are a web developer you probably have… developed a love-and-hate relationship with JavaScript.

While it is a feature-rich and constantly evolving language, it has some limitations. Especially when it comes to complex applications it may fall short.

A popular solution chosen among developers is using a different language that gets compiled to JavaScript. This can be achieved with a tool called transpiler.
A transpiler is essentially a compiler that transforms a language’s code to another high-level language code (not an assembly language).

Let us take a look at some popular language choices. I have to mention though that this is by no means an exhaustive list.

Additional languages you can keep an eye on are : ClojureScript, Racketscript, Scala.js, PureScript, Reason.

## TypeScript

By definition, “TypeScript is JavaScript for application-scale development.”

TypeScript is a strongly typed, object-oriented, compiled language. It was designed by Anders Hejlsberg (designer of C#) at Microsoft.

TypeScript is both a language and a set of tools. TypeScript is a typed superset of JavaScript compiled to JavaScript. In other words, TypeScript is JavaScript plus some additional features.

### Why Use TypeScript?

The main difference - and benefit - of Typescript over JavaScript is its type system.

TypeScript will compile the code and generate compilation errors if it finds some sort of syntax errors. This helps to highlight errors before the script is run.
TypeScript comes with an optional static typing and type inference system through the TLS (TypeScript Language Service).

TypeScript also supports Object-Oriented Programming concepts like classes, interfaces, inheritance, etc.

### Code examples

```typescript
let welcome: string = "welcome to Hashnode"
let a: number = 1 ;
let fruits:string[] = ['apples', 'apricots', 'avocados'];

let add:(a:number,b:number)=>number;
add = function(a:number,b:number):number{
    return a+b;
 }
```

## Elm

Elm is a functional language that compiles to JavaScript.

It helps you make websites and web apps. It has a strong emphasis on simplicity and quality tooling.
Elm was initially designed by Evan Czaplicki as his thesis in 2012.

### Why use Elm?

Elm promises no run time exceptions - no annoying "undefined is not a function". It uses type inference to detect corner cases and help the user with what the issue might be.

Also:

* Immutability and Uni-directional data flow is baked right in
* Functional design and currying make a functional composition
* Styling system based on modern CSS in JS approaches (see styled-components)
* Performance is quite good as well - comparing it to React and Vue it seems to produce slightly-smaller bundle sizes and faster render times.

### Code examples

```elm
import Html exposing (..)

main =
  div []
    [ h1 [] [ text "My Grocery List" ]
    , ul []
        [ li [] [ text "Black Beans" ]
        , li [] [ text "Limes" ]
        , li [] [ text "Greek Yogurt" ]
        , li [] [ text "Cilantro" ]
        , li [] [ text "Honey" ]
        , li [] [ text "Sweet Potatoes" ]
        , li [] [ text "Cumin" ]
        , li [] [ text "Chili Powder" ]
        , li [] [ text "Quinoa" ]
        ]
    ]
```

## ReScript

[ReScript](https://rescript-lang.org/) (formerly _ReasonML_) is the brainchild of React framework creator Jordan Walke. Although the language has only existed since 2016, an entire team is now working on its further development. Besides Facebook and financial giant Bloomberg, volunteer enthusiasts from all over the world are involved.

Surprisingly, however, ReScript is not a completely new language. The underlying [OCaml](https://ocaml.org/) has been around since 1996, and Walke noticed that OCaml was a good fit for React, but the unfamiliar syntax put off many front-end developers.
So he came up with the idea: How about giving the OCaml language a syntax that allows JavaScript developers to quickly find their way around? Thus, ReScript allows the concepts of a mature functional programming language with the popular [Hindley-Milner type system](https://en.wikipedia.org/wiki/Hindley%E2%80%93Milner_type_system) to be transferred to the frontend in a very short time.

The idea of ReScript is to consolidate these tools into something a little more coherent so as a developer you’re not trying to figure out how OCaml, BuckleScript, and Reason fit together.

### Why use ReScript?

What does ReScript do differently?

ReScript is relatively easy to learn for JavaScript and TypeScript developers.
The language comes with an excellent type system, high performance, and concepts from functional programming. For such a young language, there is also already relatively sophisticated tooling available

Here are a couple more selling points:

#### Build Performance

ReScript is fast to compile. If you’re used to lengthy Webpack builds that we’ve come to expect of modern tooling, ReScript will look like lighting. The build system is capable of handling projects of very large sizes quite quickly.

#### TypeScript generation

This is an interesting feature of ReScript since it does not lock you in the ecosystem. GenType is a code generation tool that lets you export ReScript values and types to use in your JavaScript or Typescript code. Handy.

### Code examples

```reason
let greetByName = (possiblyNullName) => {
  let optionName = Js.Nullable.toOption(possiblyNullName)
  switch optionName {
  | None => "Hi"
  | Some(name) => "Hello " ++ name
  }
}
```

## CoffeeScript

CoffeeScript is developed by Jeremy Ashkenas. It was first committed in Git On December 13, 2009.

Originally the compiler of CoffeeScript was written in Ruby language.
In March 2010, the CoffeeScript compiler was replaced; this time instead of Ruby, they used CoffeeScript itself.

CoffeeScript is a lightweight language based on Ruby and Python which transcompiles (compiles from one source language to another) into JavaScript.

It provides better syntax avoiding the quirky parts of JavaScript, still retaining the flexibility and beauty of the language.

### Why use CoffeeScript?

* Easily understandable − CoffeeScript is a shorthand form of JavaScript, its syntax is pretty simple compared to JavaScript. Using CoffeeScript, we can write clean, clear, and easily understandable codes.
* Write less do more − For a huge code in JavaScript, we need comparatively a very less number of lines of CoffeeScript.
* Reliable − CoffeeScript is a safe and reliable programming language to write dynamic programs.
* Readable and maintainable − CoffeeScript provides aliases for most of the operators which makes the code readable. It is also easy to maintain the programs written in CoffeeScript.
* Class-based inheritance − Unlike JavaScript, we can create classes and inherit them in CoffeeScript. In addition to this, it also provides instance and static properties as well as mixins. It uses JavaScript's native prototype to create classes.
* No var keyword − There is no need to use the var keyword to create a variable in CoffeeScript, thus we can avoid accidental or unwanted scope deceleration.
* Avoids problematic symbols − There is no need to use the problematic semicolons and parenthesis in CoffeeScript. Instead of curly braces, we can use whitespaces to differentiate the block codes like functions, loops, etc.
* Extensive library support − In CoffeeScript, we can use the libraries of JavaScript and vice versa. Therefore, we have access to a rich set of libraries while working with CoffeeScript.

### Code examples

```coffeescript
# Assignment:
number   = 42
opposite = true

# Conditions:
number = -42 if opposite

# Functions:
square = (x) -> x * x

# Arrays:
list = [1, 2, 3, 4, 5]

# Objects:
math =
  root:   Math.sqrt
  square: square
  cube:   (x) -> x * square x

# Splats:
race = (winner, runners...) ->
  print winner, runners

# Existence:
alert "I knew it!" if elvis?

# Array comprehensions:
cubes = (math.cube num for num in list)
```

# Fable

Fable is a compiler that lets you use F# to build applications that run in the JavaScript ecosystem.

F# (pronounced f-sharp) is a strongly typed Functional programming language that is already used on the server for web and cloud apps, and it's also used quite a lot for data science and machine learning. It's a great general-purpose language, and also a great fit for building beautiful UIs that run in the browser.

### Why use Fable?

F# is a great choice to build beautiful apps that run in the browser. F# is:

* Succinct with lightweight syntax
* Robust with a great type system and pattern matching
* Safe with immutability baked into the language
* Supported by large companies (such as Microsoft and Jetbrains) and comes with commercial tooling support
* When compared with JavaScript, F# is safer, more robust, and more pleasant to read and write.

F# is a mature language with functional programming and object programming capabilities, but it doesn't sacrifice readability or simplicity to offer these things.

Because of that, it can be a great choice for your next JavaScript application.

### Code examples

```fsharp
let sampleFunction1 x = x*x + 3
let result1 = sampleFunction1 4573

printfn "The result of squaring the integer 4573 and adding 3 is %d" result1

let square x = x * x

/// Adds 1 to a value.
let addOne x = x + 1

    /// Tests if an integer value is odd via modulo.
let isOdd x = x % 2 <> 0

    /// A list of 5 numbers.  More on lists later.
let numbers = [ 1; 2; 3; 4; 5 ]

    /// Given a list of integers, it filters out the even numbers,
    /// squares the resulting odds, and adds 1 to the squared odds.
let squareOddValuesAndAddOne values =
let odds = List.filter isOdd values
let squares = List.map square odds
let result = List.map addOne squares
result

printfn "processing %A through 'squareOddValuesAndAddOne' produces: %A" numbers (squareOddValuesAndAddOne numbers)
```