---
title: The Basic Formatting 
weight: 3
---

#### Basic Formatting

A single placeholder is used when it is required to print a single value.

```rust
fn main() {
    println!("Number: {}", 1);
}
```

We can use multiple placeholders within the `println!()` macro. The number of placeholders should be equal to the number of values to be printed.

```rust
fn main() {
    println!("{} is a {} Community", "Join", "CloudNativeFolks");
}
```

If we want to convert the value to binary, hexadecimal, or octal write:

```rust
{:b},{:x},{:o}
```

In the placeholder for binary, hexadecimal, or octal respectively and in the value specify the number. You can use all three of them or one of them in a single expression.

```rust
fn main() {
    println!("Number : 10 \nBinary:{:b} Hexadecimal:{:x} Octal:{:o}", 10, 10, 10);
}
```

If we want to convert the value to binary, hexadecimal, or octal write:

```rust
{:b},{:x},{:o}
```

In the placeholder for binary, hexadecimal, or octal respectively and in the value specify the number. You can use all three of them or one of them in a single expression.

```rust
fn main() {
    println!("Number : 10 \nBinary:{:b} Hexadecimal:{:x} Octal:{:o}", 10, 10, 10);
}
```

We can perform basic math and the placeholder gets replaced with the result.

```rust
fn main() {
    println!("{} + {} = {}",10, 10, 10 + 10);
}
```

#### Placeholder for debug trait

```rust
fn main() {
    println!("{:?}", ("This is a Rustlabs", 101));
}
```

## Knowledge check 

{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---


## What is the output of the following code?

```
fn main() {
    println!("Enhance your coding skills from {1} courses.  {0} courses are very {1}", "rustlabs", "interactive");
}
```

- [ ] Enhance your coding skills from kubedaily courses. kubedaily courses are very interactive <br>
- [ ] Enhance your coding skills from interactive courses. kubedaily courses are very interactive <br>


## What is the output of the following code?

```
fn main() {
    println!("{}{}", 2, 1);
}
```
- [ ] 21 
- [ ] 12

{{</quizdown>}}
