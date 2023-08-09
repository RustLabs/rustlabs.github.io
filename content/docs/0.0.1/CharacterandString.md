---
title: Character and String
weight: 11
---

# Character and String

- Character 

The variable is used to store a single character value, such as a single digit or a single alphabet. The value assigned to a char variable is enclosed in a single quote('') .

> Note: Unlike some other languages, a character in Rust takes up 4 bytes rather than a single byte. It does so because it can store a lot more than just an ASCII value like emojis, Korean, Chinese, and Japanese characters.


![](/img/diagrams/15.my_char.png)


# Example 

The code below defines a character both explicitly and implicitly:

- Explicit Definition 

The following code explicitly defines the variable using the char keyword:

```
fn main() {
    // explicitly define 
    let char_1:char = 'e';
    println!("character1: {}", char_1); 
}

```

Output

```
character1: e
```

Implicit Definition 

The following code implicitly defines the character type of the variable by assigning the single value enclosed within single quotes to them.

```
fn main() { 
    // implicitly define
    let char_2 = 'a';
    let char_3 = 'b';
    println!("character2: {}", char_2);
    println!("character3: {}", char_3);
}

```

Output

```
character2: a
character3: b

```

# String 

A string is any sequence of characters enclosed within double quotes (" ").

![](/img/diagrams/16.my_char_string.png)


# Example 

The code below defines a string both explicitly and implicitly:

- Explicit Definition 

The following code explicitly defines the variable using the `&str` keyword:

```rust
fn main() {
    // explicitly define 
    let str_1:&str = "Rust Programming";
    println!("String 1: {}", str_1); 
}

```

Output

```bash
String 1: Rust Programming
```

# Implicit Definition 

The following code implicitly defines the string type of the variable by assigning the single value enclosed within double quotes to them.

```rust
fn main() { 
    // implicitly define
    let str_2 = "Rust Programming";
    println!("String 2: {}", str_2);
}

```
output:- 

```bash
String 2: Rust Programming

```

# Quiz 

Test your understanding of Character and String in Rust!

{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---


# What is the output of the following code? <br>

```rust
let value:str = "Rust Programming";
println!("{}", value);

```

- [ ] Rust Programming 
- [ ] Error 

#  What is the valid syntax for defining a character explicitly? 

 - [ ] let char1 : char = 'e';    
 - [ ] let char1: character = 'e'; 

{{</quizdown>}}




