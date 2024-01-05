---
title: Logical Operators
weight: 17
---

# Logical Operators


# What Are Logical Operators? 
Logical operators operate on true / false values

![](/img/diagrams/27.logical-op.png)

# Types 

The following table summarizes the types and functions of the logical operators:


| operator  	| operation  	| explanation 	|
|-	|-	|-	|
| operand1 && operand2 	| AND 	| Evaluates to true if operand 1 and Operand 2 both evaluates to be true   	|
| operand1 \|\| operand2  	| OR 	| Evaluates to true if operand 1 or Operand 2 true evaluates to be true 	|
|     ! operand1   	| NOT 	| negates the value of single operand  	|


The logical AND and OR are known as Lazy Boolean expressions because the left-hand side operand of the operator is first evaluated. If it is false, there is no need to evaluate the right-hand side operand in 
case of AND. If it is true, there is no need to evaluate the right-hand side operand in case of OR.

The following example shows the use of logical operators in a program:

```
fn main() {
  let a = true;
  let b = false;
  println!("Operand 1:{}, Operand 2:{}", a , b);
  println!("AND:{}", a && b);
  println!("OR:{}", a || b);
  println!("NOT:{}", ! a);
}


```
output:- 

```
Operand 1:true, Operand 2:false
AND:false
OR:true
NOT:false


```

# Quiz

Test your understanding of logical operators in Rust!

{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---


##  What is the output of the following code?

```
fn main() {
  let mut a = false;
  let mut b = true;
  a = a && b || ( ! a);
  b = !b;
  println!("a:{}", a);
  println!("b:{}", b); 
}


```

- [ ] ```
     a:false 
     b:true 
    ``` 

- [ ] ```
    a:true 
    b:false  
   ```

- [ ] ```
   a:true 
   b:true  
   ```

- [ ] ```
    a:false  
    b:false 
    ```

{{</quizdown>}}    