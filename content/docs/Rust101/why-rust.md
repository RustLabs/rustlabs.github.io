---
title: Why Rust?
icon: "❓"
weight: 1
---

Rust continues to top the charts as the most admired and desired language by developers, and we are going to learn deeper into how (and why) with hands on Rust is stealing the hearts of developers around the world.

> Rust has been said to be named after a particularly robust type of fungi that is “over-engineered for survival,” according to Hoare.

### What is Rust?

Initially designed to offer a more secure option compared to C and C++, Rust is a programming language focused on systems development that has become increasingly popular among programmers. Its primary attributes include an emphasis on safety, efficiency, and productivity. Being a statically typed language, Rust ensures that types for variables and expressions are established and verified during compilation. This approach enhances memory safety and improves error identification, leading to more dependable and reliable software builds


Rust is a programming language designed to enable everyone to develop software that is both dependable and efficient. The creation of Rust began with Graydon Hoare and a team of collaborators in 2006, during Hoare's tenure at Mozilla Research. The language captured significant attention and acquired a growing user base, leading to Mozilla's decision in 2010 to officially sponsor its development efforts

[Stack Overflow Survey 2023](https://survey.stackoverflow.co/2023/#section-admired-and-desired-programming-scripting-and-markup-languages)

### Why Is Rust Different? 
 - Speed <br>
 - Cargo Package Manager <br>
 - Error Reporting <br>
 - Effective C Integration <br>
 - Fearless Concurrancy without Data Races <br>
 - Guranteed Memory Safety without Garbage Collection
 
- There are many reasons why Rust is different from other programming languages.

### Speed 

Rust's design allows for abstraction without runtime penalties, ensuring that code remains both high-quality and readable. This unique approach ensures efficiency, as runtime costs are incurred only for the specific features employed in the code.

### Guranteed Memory Safety without Garbage Collection

**Ownership and Borrowing for Memory Safety** : Rust ensures memory safety without a garbage collector by utilizing a unique system of ownership and borrowing, controlling how memory is accessed and managed.

**Safe Code by Design**: Unlike C and C++, Rust is designed to write inherently safe code, with the language itself managing object lifecycles from creation to destruction.

**Automatic Memory Management** : In Rust, the correct amount of memory is allocated for objects and then automatically deallocated by the system when they are no longer needed, streamlining memory management.

### Cargo Package Manager in Rust

**Standardized Package Management**: Unlike system languages such as C and C++, Rust comes with a built-in package manager, Cargo, which centralizes access to a wide range of Rust libraries and frameworks.

**Facilitating Application Development and Code Distribution**: Cargo aids developers in creating impressive applications and simplifies the process of distributing code to end-users, enhancing the overall development workflow in Rust.

### Error Reporting in Rust

**Color-Coded Clarity** : Rust enhances error message visibility by displaying them in color, making them easier to identify and understand.

**Intelligent Suggestions** : The compiler often provides suggestions for fixing formatting errors and typos, offering a more intuitive coding experience.

**Detailed Error Information** : Rust goes beyond just indicating the line with an error; it also specifies the error type, aiding in quicker and more effective debugging.

### Efficient C Binding 

**C Language Interoperability**: Rust supports seamless integration with C, featuring a foreign function interface (FFI) that allows communication with C APIs.

**Memory Safety Assurance**: Thanks to its stringent ownership rules, Rust ensures memory safety even when interfacing with C, enhancing reliability and security.


#### Fearless Concurrancy without Data Races

**Preventing Data Races** : Rust effectively prevents data races, a scenario where multiple threads access the same memory location simultaneously, by employing its unique ownership model


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

