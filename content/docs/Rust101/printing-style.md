---
title: Printing Styles
weight: 4
---

- The table below summarizes the macros used to print in Rust.


| macro 	| Printing Style  	|
|-	|-	|
| print!() 	| prints strings to console  	|
| println!() 	| same as print!() but also appends new line character at end of string 	|
| eprint!() 	| prints anything within the parentheses as an error 	|
| eprintln!() 	| same as eprint!() but also appends new line character at end  	|


Let’s discuss each of the macros in detail.

 




The print!() macro simply prints the output to the console.
## Example 
The following example prints “Rust Programming Course” in one line

```
fn main() {
    print!("Rust Programming");
    print!(" Course");
}

```

- println!() 

The println!() macro appends a new line at the end of the string.
# Example 

The following example prints “Rust Programming” on one line and “Course” on the new line.

```
fn main() {
    println!("Rust Programming");
    println!("Course");
}

```
# eprint!() 

The eprint!() macro displays the output as an error.

# Example 

The following example prints “Rust Programming” and “Course” on the same line but as an error.

```
fn main() {
    eprint!("Rust Programming");
    eprint!(" Course");
}


```
# eprintln!() 

The eprint!() macro displays the output as an error and appends a new line(\n) at the end of it.
# Example 

The following example prints “Rust Programming” as an error and appends a new line to it. Then prints “Course” and appends a new line.

```
fn main() {
    eprintln!("Rust Programming");
    eprintln!("Course");
}


```
📝Note: eprint!() and eprintln!() come in handy when we want to indicate to the user that an error condition has occurred.

# Quiz 


{{<quizdown>}}
---
primary_color: orange
secondary_color: lightgray
text_color: black
shuffle_questions: false
---

## Which of the following print statement appends a new line to the output? 

- [ ] `print!("Rust");` 
- [ ] `println!("Rust");`
- [ ] `eprint!("Rust");` 
- [ ] `eprintln!("Rust");`


##  Which of the following is used to display an error?

- [ ] `eprint!("Rust");`
- [ ] `eprintln!("Rust");`
- [ ] `print!("Rust");`
- [ ] `println!("Rust");`

{{</quizdown>}}






