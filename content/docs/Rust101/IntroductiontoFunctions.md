---
title: Introduction to Functions
weight: 35
---


Introduction to Functions

- What Is a Function? 

A function is a block of code that can be reused. It is used to perform some specific tasks.

-  main Function 

The simplest possible function that we have studied so far is the main function that is declared with fn keyword. This is where the program execution starts.

However, it is possible to define a user-defined function.
    
- User-defined Functions

The functions that are customized and are written by the programmer to perform the specified tasks.

# Define a Function
A function is declared with the fn keyword.

- Syntax 
The general syntax is :

![](/img/diagrams/66.fn-syntax.png)

- Naming Convention: The convention for writing a function name is in a snake case, i.e.,
  - All letters should be lower case
  - All words should be separated by underscores
  
  
# Call a Function 
The function executes when it is invoked.

- Syntax 

The expression starts with the function name followed by the round brackets and then the semicolon. The function parameters may be added between the parentheses if needed.

The general syntax for invoking a function:

![](/img/diagrams/67.invoke_fn.png)

 Note: A user-defined function can be invoked from another function or the main function. It can be defined anywhere, above or below the main function.

If a function is invoked but its definition does not exist, the compiler will throw a compilation error, ❌, such as 
error[E0425]: cannot find function function_xyz in this scope.

# Example 
The following example makes a user-defined function and invokes it from within the main function.

```
//define a function
fn display_message(){
  println!("Hi, this is my user defined function");
}
//driver function
fn main() {
     //invoke a function
      display_message();
      println!("Function ended");
}


```
Output

```
Hi, this is my user defined function
Function ended
```
# Explanation

The above program comprises two functions, the user-defined function display_message() and the driver function main() where the function is being called.

- User defined function 

The function `display_message()` is defined from line 2 to line 4. On line 3 a message is printed.

- Driver function 

The driver `function main()` is defined from line 6 to line 10. On line 8 the function `display_message()` is invoked.

# Quiz 

Test your understanding of basics of functions in Rust!

{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---


# What is the output of the following program?

```
fn display_message(){
    println!("Hi this is my user defined function");
}
fn main() {
    display_message();
    println!("function is called");
}

```

- [ ] Hi, this is my user defined function 
      function is called  

- [ ] Hi, this is my user defined function 


{{</quizdown>}}








