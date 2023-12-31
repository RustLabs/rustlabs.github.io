---
title: Match Expression
weight: 26
---

# Match Expression

# What Is a match Expression? 

Match expression checks if the current value corresponds to any value within the list of values.
Match expression are similar to switch statement in languages like C and C++. They give a more compact code when compared with the if/else construct.

- Syntax 
Match expression uses a match keyword.
The match expression can be written in two different ways, which are given below:

- Method 1: 
If you do not want to assign a value to the result variable from within the match block

![](/img/diagrams/51.match_ex1.png)

```
fn main() {
    // define a variable 
    let x = 5;
    // define match expression
    match x {
        1 => println!("Java"),
        2 => println!("Python"),
        3 => println!("C++"),
        4 => println!("C#"),
        5 => println!("Rust"),
        6 => println!("Kotlin"),
        _ => println!("Some other value"),
    };
}

```
output:- 

```
Rust
```

# Method 2: 
If you want to assign a value to the result variable from within the match block

![](/img/diagrams/52.match_ex2.png)

```
fn main(){
   // define a variable
   let course = "Rust";
   // return value of match expression in a variable
   let found_course = match course {
      "Rust" => "Rust",
      "Java" => "Java",
      "C++" => "C Plus Plus",
      "C#" => "C Sharp",
      _ => "Unknown Language"
   };
   println!("Course name : {}",found_course);
}

```
output:- 

```
Course name : Rust

```

# Quiz 
Test your understanding of match expression in Rust.

{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---


# What is the output of the following code?


```
fn main() {
  let x = 21;
 
  match x {
      1 => println!("Java"),
      2 => println!("Python"),
      3 => println!("C++"),
      4 => println!("C#"),
      5 => println!("Rust"),
      6 => println!("Kotlin"),
      _ => println!("Some other value"),
  }
}


```
- [ ] Python <br> 
   Java <br>
- [ ] Some other value <br>

# What is the output of the following code?

```
fn main() {
  let mut x = 2;
  match x {
      1 => println!("Java"),
      2 => println!("Python"),
      3 => println!("C++"),
      4 => println!("C#"),
      5 => println!("Rust"),
      6 => println!("Kotlin"),
      _ => println!("Some other value"),
  }
  x = 1;
  match x {
      1 => println!("Java"),
      2 => println!("Python"),
      3 => println!("C++"),
      4 => println!("C#"),
      5 => println!("Rust"),
      6 => println!("Kotlin"),
      _ => println!("Some other value"),
  }
}


```

- [ ] Python <br>
   Java <br>
   
- [ ] Some other value <br>

- [ ] Java <br>
   Python <br>


{{</quizdown>}}
   



