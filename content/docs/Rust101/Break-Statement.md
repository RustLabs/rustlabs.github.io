---
title: Break Statement
weight: 31 
---

# Break Statement

# What Is a `break `Statement? 

The break statement terminates the loop. It is generally placed inside a conditional statement so that the loop terminates if the associated condition is true.

![](/img/diagrams/61.break_flow.png)

Break statement is valid in case of while, for and loop.
# Using With a for Loop 

Below is an example of break expression, using a for loop.
- The range defined in the for loop is from 0 to 10.
- Within the for loop :
    - The value of `i ` is printed
    - When the value of ` i ` is equal to ` 5 `, the loop terminates
    
```
fn main() {
  // define a for loop
  for i in 0..10 {
    println!("i:{}", i);
    if i == 5 {
      break;
    }
  }
}
```
output 

```
i:0
i:1
i:2
i:3
i:4
i:5

```

# Using With a while Loop 

Below is an example of break expression, using a while loop.
 - A mutable variable i is defined
 - A boolean variable found is defined
  Within the while loop body :
     -  The value of i is printed
     -  When the value of `i` is equal to` 5`, the loop terminates
     
```
fn main() {
  let mut i = 1;
  let found = false;
  // define a while loop
  while !found {
    println!("i:{}", i);
    if i == 5 {
      break;
    }
    i = i + 1;    
  }
}



```
output

```
i:1
i:2
i:3
i:4
i:5

```

# Using With a loop 

Below is an example of break expression, using a loop.
 - A mutable variable i is defined
 - Within the loop body:
      -  The value of i is printed
      -  When the value of `i ` is equal to ` 4 `, the loop terminates

 The infinite loop is turned into a “manageable” loop.
 
 ```
 fn main() {
  let mut i = 1;
  // define a loop
  loop{
    println!("i:{}", i);
    if i == 5 {
      break;
    }
    i = i + 1;    
  }
}
 
 ```
Output

```
i:1
i:2
i:3
i:4
i:5

```

# Quiz 

Test your understanding of how break statement works in Rust.

{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---

# How many times does the print statement in the loop run?

```
fn main() {
  for i in 0..10 {
    println!("i:{}", i);
    if i == 5 {
      break;
    }
  }
}

```

- [ ] 5
- [ ] 6
- [ ] 7

{{</quizdown>}}

     




