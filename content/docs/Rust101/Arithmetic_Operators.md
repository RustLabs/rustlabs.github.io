---
title: Arithmetic Operators
weight: 16
---

# Arithmetic Operators

- What Are Arithmetic Operators?
    - Arithmetic operators are used to perform arithmetic operations.
    
- Types 
The table below summarizes the arithmetic operations in Rust.
![](/img/diagrams/26.arth-op.png)


# Types
The table below summarizes the arithmetic operations in Rust.

| operator  	| operation  	| explanation 	|
|-	|-	|-	|
| operand1 + operand2 	| addition 	| add operand1 and operand2  	|
| operand1 - operand2  	| subtraction 	| subtract operand2 from operand1 	|
| operand1 / operand2 	| divide 	| divide operand1 by operand2 	|
| operand1 * operand2 	| multiplication 	| multiply operand1 with operand2 	|
| operand1 % operand2 	| modulus 	| get reminder of operand1 by dividing with operand2  	|
    

The following example shows the use of arithmetic operators in a program:

```
fn main() {
    let a = 4;
    let b = 3;
    
    println!("Operand 1:{}, Operand 2:{}", a , b);
    println!("Addition:{}", a + b);
    println!("Subtraction:{}", a - b);
    println!("Multiplication:{}", a * b);
    println!("Division:{}", a / b);
    println!("Modulus:{}", a % b);
}

```

output:

```
Operand 1:4, Operand 2:3
Addition:7
Subtraction:1
Multiplication:12
Division:1
Modulus:1

```

# Quiz 

Test your understanding of arithmetic operators in Rust!

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

```rust
fn main() {
  let mut a = 4;
  let mut b = 3;
  a = a + b;
  a = a * b;
  a = a - b;
  b = b - a;
  println!("a:{}", a);
  println!("b:{}", b);
   
}

```
- [ ]  a:18  
       b:-15 
   
- [ ] a:15 
      b:18 
   
- [ ] a:18 
      b:15 
   

{{</quizdown>}}   