---
title: Why Rust?
weight: 1
---

### What is Rust?

Rust is a language empowering everyone to build reliable and efficient software. rust created by Graydon Hoare and many others around 2006 while Hoare was working at Mozilla Research. It gained enough interest and users that by 2010 Mozilla had sponsored the development efforts

https://survey.stackoverflow.co/2022/#technology-most-loved-dreaded-and-wanted

StackOverflow 2022 - it's the seventh year as the most loved programing language with 87% of developers saying they want to continue using it.


[](https://cdn.hashnode.com/res/hashnode/image/upload/v1671036539634/C7R8KV-3-.png align="center")

the language is syntactically similar to C, so you'll find things like for loops, semicolon-terminated statements and curly braces denoting block structures, Rust can guarantee memory safety through the use of a borrow checker that tracks which part of a program has safe access to a different part of memory. This track does not come at the expense of performance, though. Rust programs compile to native binaries and often match or beat the speed of programs written in c or c++ for this reason, Rust is often described as a system programing language that has been designed for performance and safety.




## Why Is Rust Different? <br>
 - Speed <br>
 - Safety <br>
 - Cargo Manager <br>
 - Error Messages <br>
 - Efficient C Binding <br>
 - Threads without Data Races <br>


# Why Is Rust Different? 
 
- There are many reasons why Rust is different from other programming languages.

# Speed 

Rust pays no penalty for the abstraction and only pays for the features that are actually used. This improves the code quality and readability without affecting the run time cost.

# Safety 

- Rust does not have a garbage collector. It ensures memory safety using ownership and its borrowing concept 

- The most significant difference between C, C++, and Rust is writing safe code. 
- In Rust, the objects are managed by the programming language from the beginning to the end. 
- The proper amount of memory required is allocated
and automatically deallocated by the system when it is no longer in use.


# Cargo Manager 

- System languages like C and C++ never had a standard package manager. Rust provides a cargo manager that has all the

- rust libraries and frameworks to not only help developers make fantastic applications, but also distribute code to end-users.

# Error Messages 

The error messages in Rust are displayed using color. Formatting and misspellings in the program are commonly suggested.
It not only displays the line which has the error but, also the type of error.

# Efficient C Binding 

The Rust language can interoperate with the C language. It provides a foreign function interface to communicate with C API’s. 
Due to its ownership rules, it can guarantee memory safety.


# Threads without Data Races 

Data race is a condition where two or more threads can access the same memory location. Rust uses the concept of ownership to avoid data races.


#### To start, You'll need to install Rust

one of the easy ways to install, upgrade, and manage Rust using

the rustup tool .it works equally well on Windows, Linux or macOS.

```bash
 curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

if you have already installed `rustup` , you might want to run `rustup update` to get the latest version of the language and tools, as Rust updates in about six weeks. execute `rustup doc` to read volumes of documentation. you can check your version of `rustc` compiler with the following command.

```bash
rustc --version 
rustc 1.68.0-nightly (b70baa4f9 2022-12-14)
```

