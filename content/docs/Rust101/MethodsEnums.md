---
title: Methods of Enums
weight: 59
---


# Methods of Enums

- What Are Methods? 
Just like structs, methods are functions specific to enums.

- Syntax 

To define methods of `enum` write the functions within the `impl` followed by the `enum` name and then the functions within the `impl` block.

![](/img/diagrams/103.enum-method.png)


 - Move `enum` related logic in the `impl` construct
 
- Example 
The example below declares an `enum`, named `TrafficSignal` and defines an enum method `is_stop` within the `impl` construct:

```
#![allow(dead_code)]
#[derive(Debug)]
// declare an enum
enum TrafficSignal{
  Red, Green, Yellow
}
//implement a Traffic Signal methods
impl TrafficSignal{
  // if the signal is red then return
   fn is_stop(&self)->bool{
     match self{
       TrafficSignal::Red=>return true,
       _=>return false
     }
   }
}
fn main(){
  // define an enum instance
  let action = TrafficSignal::Red;
  //print the value of action
  println!("What is the signal value? - {:?}", action);
  //invoke the enum method 'is_stop' and print the value
  println!("Do we have to stop at signal? - {}", action.is_stop());
}

```
Output

```
What is the signal value? - Red
Do we have to stop at signal? - true

```


# Quiz 

Test your understanding of methods of enum in Rust.

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
#![allow(dead_code)]
#[derive(Debug)]
enum TrafficSignal {
  Red, Green, Yellow
}
impl TrafficSignal{
   fn is_stop(&self)->bool{
     match self{
       &TrafficSignal::Red=>return true,
       _=>return false
     }
   }
}
fn main(){
  let action = TrafficSignal::Yellow;
  println!("What is the signal value? - {:?}", action);
  println!("Do we have to stop at signal? - {}", action.is_stop());
}

```

- [ ] What is the signal value? - Yellow
      Do we have to stop at signal? - false

- [ ] What is the signal value? - Red
      Do we have to stop at signal? - true


{{</quizdown>}}



