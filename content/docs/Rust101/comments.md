---
layout: documentation
title: comments
weight: 5
doctype: Rust101
---


# Comments

Comments are programmer readable instructions to help explain things about your code. The compiler ignores them.

# Types of Comments in Rust 

Rust has two types of comments that are commonly used:

## Line Comments `// `

The comments followed by a double forward slash, `//`, are known as line comments.

This is the most recommended style of comment for commenting a single line.

```
// Writing a Rust program
fn main() {
    //The line comment is the recommended comment style
    println!("This is a line comment!"); // print hello World to the screen
}

```
# Block Comments `/*...*/` 

Text enclosed within `/*...*/` is known as a block comment.

This is used for temporarily disabling a large chunk of code.


# Doc Comments 

The comments followed by `///` or `//! `are known as doc comments. Let’s see the difference between the two sets of doc comments.

# Outer Doc Comments `/// `

Outer doc comments are written outside the block of code.

This type of comment supports markdown notation. This is used to generate docs referring to the following item.

# Inner Doc Comments `//! `

Inner doc comments are written inside the block of code.

This comment style is used to generate docs referring to the item within a block of code.

```
/// This is a Doc comment outside the function
/// Generate docs for the following item.
/// This shows my code outside a module or a function
fn main() {
    //! This a doc comment that is inside the function   
    //! This comment shows my code inside a module or a function  
    //! Generate docs for the enclosing item
    println!("{} can support {} notation","Doc comment","markdown");
}

```

# Quiz 

{{<quizdown>}}

---
primaryColor: steelblue
shuffleQuestions: false
shuffleAnswers: true
---


# 1.Which type of comment is this? `//`

  - [ ] Line
  - [ ] Doc
  
# 2.Which comment supports markdown notation?

 - [ ] Line comment
 - [ ] Doc comment

{{</quizdown>}}

