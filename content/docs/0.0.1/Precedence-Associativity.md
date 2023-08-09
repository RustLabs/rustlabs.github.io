---
title: Precedence and Associativity
weight: 23
---

# Precedence and Associativity

# Precedence

The precedence of an operator determines which operation is performed first in an expression with more than one operators.

Operators are listed below in the order of their precedence from highest to lowest :

- Unary
   - Logical/Bitwise NOT - `!`
   - Derereference - `*`
   - Borrow - `&`, `&mut`
   
   
- Binary
   - Typecast - `as`
   - Multiplication- `*`,Division - `/`,Remainder- `%`
   - Addition - `+`, Subtraction -` -`
   - Left Shift - `<<`, Right Shift - `>>`
   - Bitwise AND - `&`
   - Bitwise XOR - `^`
   - Bitwise OR - `|`
   - Comparison - `==` `!=` `<`` >` `<= ``>=`
   - Logical AND - `&&`
   - Logical OR - `||`
   - Range - `start .. stop`
   - Assignment/Compound Assignment - `= += -= *= /= %= &= |= ^= <<= >>=`
   
   
 Note: The operators that are written in the same row have the same order of precedence.
 
# Associativity 

If two or more operators of the same precedence appear in a statement, then which operator will be evaluated first is defined by the associativity.

# Left to Right Associativity 

Left associativity occurs when an expression is evaluated from left to right. An expression such as` a ~ b ~ c`, in this case, would be interpreted as 
`(a ~ b) ~ c` where `~ `can be any operator.
The operators below can be chained as left associative.

📝The comparison, assignment, and the range operator cannot be chained at all.

# Example 1 

The example below solves an expression according to its operator precedence:

```
fn main() {
    println!("Answer : {}",( 3 + 5 ) * 9 / 7 & 8);
}

```
output:- 
```
Answer : 8

```

![](/img/diagrams/39.precedence-ex1.png)

# Example 2 

The example below solves an expression according to its operator precedence:

```
fn test() {
    println!("{}", 2 + 3 / 5 ^ 7 & 8 | 9);
}

```
output:
```
11

```

![](/img/diagrams/40.precedence-ex2.png)

# Quiz 

Test your understanding of operator precedence in Rust!

{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---


# What is the output of the following code according to its operator precedence in Rust? 


```
fn main() {
    println!("{}", 3 + 4 - 9 / 6 * 6 ^ 8 & 3);
}

```

- [ ] 1 
- [ ] 2 
- [ ] 3 
- [ ] 4 



{{</quizdown>}}



   

