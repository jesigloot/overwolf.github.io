---
id: type-definition-file
title: Overwolf Type Definition File
sidebar_label: Type Definition File
---

:::important
Even if your application not uses TypeScript at all, you can use the type definition files for autocompletion and documentation purposes. More details [here](#using-overwolfdts-file).
:::

**You can find the Overwolf API ts definition file [here](https://github.com/overwolf/community-gists/tree/master/typescript)**

## TypeScript overview

TypeScript is a superset of JavaScript which adds optional static typing to the language, hence its name. Static typing enables the compiler to check that operations performed on variables are legal. Those checks prevent you from attempting to invoke a number as a function, for example.

TypeScript can help us to avoid painful bugs that developers commonly run into when writing JavaScript by type-checking the code. It reduces bugs like null handling, undefined, etc. Strongly typed characteristics restrict developers to write type-specific code with proper checks.

In order for TypeScript to perform the type checking, the types need to be defined somewhere. It's pretty straightforward how to add type definitions to the variables declared in your own code:

```js
//  anyObject hold values of any arbitrary type
var anyObject: any;

// count is a number
var count: number;


// regexPatterns is an array of regular expressions
var regexPatterns: RegExp[];

// reverse is a function which accepts and returns a string
var reverse: (input: string) => string;
```

but how does TypeScript know about the types of variables and functions of existing JavaScript libraries? This is where type definition files come into play.

## TypeScript definition files overview

Type definition files allow you to provide type information for JavaScript code that is by itself (by its very nature) not statically typed. The file extension for such a file is “d.ts”, where d stands for definition. Type definition files make it possible to enjoy the benefits of type checking, autocompletion, and member documentation.


## Using overwolf.d.ts file

Even if your application uses plain JavaScript and no TypeScript at all, you can use the type definition files for autocompletion and documentation purposes. Simply include them in your Visual Studio Code project.  will then include the found types in its auto-completion list, given that you've got TypeScript installed:

![alt-text](assets/def-file-demo.gif)

Of course, you won't get the benefit of type checking because you're not actually using TypeScript, but still, the provided information can be very helpful for working with the dynamic and loosely typed language that is JavaScript.

