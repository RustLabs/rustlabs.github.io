---
title: Comparison Operators
weight: 18
---

# Comparison Operators


# What Are Comparison Operators?

Comparison Operators are used for comparing the values of two operands.
![](/img/diagrams/28.camp_ops.png)


# Types 

Below is the list of comparison operators in Rust.

| operator  	| operation  	| explanation 	|
|-	|-	|-	|
| operand1 > operand2 	| greater then 	| Evaluates to true if operand 1 is greater then Operand 2   	|
| operand1 < operand2  	| lesser then 	| Evaluates to true if operand 1 is lesser then Operand 2 	|
| operand1 <= operand2   	| less then equal to 	| Evaluates to true if operand 1 is lesser or equal to the Operand 2 	|
| operand1 >= operand2 	| greater then equal to 	| Evaluates to true if operand 1 is greater or equal to the Operand 2 	|
| operand1 == operand2 	| equal to 	| Evaluates to true if operand 1 equal to the Operand 2 	|
| operand1 != operand2 	| Not equal to  	| Evaluates to true if operand 1 not equal to the Operand 2 	|

The following example shows the use of comparison operators in a program:

```
fn main() {
    let a = 2;
    let b = 3;
    println!("Operand 1:{}, Operand 2:{}", a , b);
    println!("a > b:{}", a > b);
    println!("a < b:{}", a < b);
    println!("a >= b:{}", a >= b);
    println!("a <= b:{}", a <= b);
    println!("a == b:{}", a == b);
    println!("a != b:{}", a != b);
}

```
output:- 

```
Operand 1:2, Operand 2:3
a > b:false
a < b:true
a >= b:false
a <= b:true
a == b:false
a != b:true

```

# Quiz 

Test your understanding of comparison operators in Rust!
   
{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---


Test your understanding of comparison operators in Rust!


# What is the output of the following code?

```
fn main() {
  let mut a = true;
  let mut b = true;
  a = a > b && b < a;
  b = !b;
  println!("a: {}", a);
  println!("b: {}", b); 
}

```

- [ ] ```
      a: false  
      b: true
    ```

- [ ] ```
    a: true 
    b: false 
   ```

- [ ] ```
    a: true  
    b: true  
    ```

- [ ] ``` 
       a: false 
       b: false 
     ```

{{</quizdown>}}