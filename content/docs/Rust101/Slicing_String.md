---
title:  Slicing a String
weight: 47
---


# Slicing a String

What Is Slicing? 
- Slicing is used to get a portion of a string value.

- Syntax
The general syntax is:
```
let slice = &string[start_index..end_index]
```
Here,

- start_index and end_index are the positions of starting and ending index of the original array respectively.
    -   Note: The start_index is inclusive and end index is exclusive
    
- `&` indicates that the variable slice borrows the string.
   -  Note: The minimum value of `start_index` is `0` and the maximum value is the size of the string
   
```
   fn main() {
   let string = "Rust Programming".to_string();
   let slice = &string[5..12]; 
   // get characters at 5,6,7,8,9,10 and 11 indexes
   println!("Slice : {}", slice);
}
   
```
output 
```
Slice : Program

```

# Quiz 

Test your knowledge of slicing a string in Rust.

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
   let string = "Rust Programming".to_string();
   let slice = &string[0..3]; 
   println!("{}", slice);
}


```
- [ ]  Rust
- [ ] Rus





{{</quizdown>}}

