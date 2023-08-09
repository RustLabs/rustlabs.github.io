---
title: boolean
weight: 10
---

# Boolean

The boolean variable can take a value either true or false.

# Example 

The following code explains how to define a boolean variable in three different ways:

- Explicit Definition

The following code explicitly defines the variable using the bool keyword:

```rust
fn main() {
    //explicitly define a bool
    let is_bool:bool = true;
    println!("explicitly_defined: {}", is_bool);
}

```
Output

```
explicitly_defined: true
```

# Implicit Definition 

The following code implicitly defines the boolean type of a variable by assigning the value true or false to the variable.

```rust
fn main() {
    // assign a boolean value
    let a = true;
    let b = false;
    println!("a: {}", a);
    println!("b: {}", b);
}

```

# Result of an Expression 

The result of an expression that evaluates to either true or false (for example a comparison of two values) can be assigned to an implicit boolean variable

```rust
fn main() {
    // get a value from an expression
    let c = 10 > 2;
    println!("c: {}", c);
}
```
Output

```rust
c: true
```


# Quiz 

Test your understanding of boolean data type in Rust!


{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---


Test your understanding of boolean data type in Rust!


# What is the output of the following code? <br> 

```rust
let value = 13 > 20;
println!("{}", value);

```

- [ ] True  
- [ ] false 

{{</quizdown>}}






