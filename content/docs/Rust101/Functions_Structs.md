---
title: Functions and Structs
weight: 53
---

# Functions and Structs
- Often, we need to pass a struct instance to a function. For example, in the previous lesson, every time we wanted to print a 
new struct instance we had to write a new print macro to print it. However, we can avoid multiple print statements by writing one print 
statement within a function and calling it when we need it.

# Pass Structs to a Function 
- The structs can be passed to a function and the function can be invoked when required.

![](/img/diagrams/90.pass-struct-fn.png)

```
//declare a struct
struct Course {
   code:i32,
   name:String,
   level:String, 
}
fn display_mycourse_info(c:Course) {
println!("Name:{}, Level:{} ,code: {}", c .name, c .level, c.code);
}
fn main() {
   //initialize
   let course1 = Course  {
      name:String::from("Rust"),
      level:String::from("beginner"),
      code:130
   };
   display_mycourse_info(course1);
    let course2 = Course  {
      name:String::from("Java"),
      level:String::from("beginner"),
      code:130
   };
   display_mycourse_info(course2);
}

```
output

```
Name:Rust, Level:beginner ,code: 130
Name:Java, Level:beginner ,code: 130

```
# Return Structs From a Function 

Structs can also be returned from the functions.

![](/img/diagrams/91.return-struct-fn.png)

```
//declare a struct
struct Course {
   code:i32,
   name:String,
   level:String, 
}
fn return_rust_course_info(c1:Course, c2:Course)-> Course{
   println!("I got into function and return values from there");
   if c1.name == "Rust" {
      return c1;
   }
   else{
      return c2;
   }
}

fn main() {
   //initialize
   let course1 = Course  {
      name:String::from("Rust"),
      level:String::from("beginner"),
      code:130
   };
    let course2 = Course  {
      name:String::from("Java"),
      level:String::from("beginner"),
      code:130
   };
  
  let choose_course = return_rust_course_info(course1, course2);
  println!("I choose to learn {} {} course with code:{}", choose_course.name, choose_course.level, choose_course.code);
}

```
output 

```
I got into function and return values from there
I choose to learn Rust beginner course with code:130
```




