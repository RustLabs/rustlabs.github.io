---
title: The 'use' Keyword
weight: 69
---


# The 'use' Keyword

![](/img/diagrams/121.use-keyword.png)


## Why Use the use Keyword?
The benefit is greatest when items in the same module need to be referred to in the code again and again.
Now, we don’t have to type the entire path over and over.


The following example shows how we can write a precise code using a use keyword:

```
pub mod chapter {
    pub mod lesson { // mod level 1
        pub mod heading { // mod level 2
            pub fn illustration() {  // mod level 3
              println!("Hi, I'm a 3rd level nested function");
            }
        }
    }
}
use chapter::lesson::heading; // make use of `use` keyword
fn main() {
    heading::illustration(); // call the function
}



```
output

```
Hi, I'm a 3rd level nested function

```

# Glob Operator `( * )`

![](/img/diagrams/122.glob-operator.png)

The glob operator helps you to prevent writing `EnumName::variant` when assigning enum value to a variable.

the following example shows how we can avoid writing a lengthy code using the glob operator `*`.

```
// make this `enum` printable with `fmt::Debug`.

#[derive(Debug)]

enum KnightMove{

   Horizontal,Vertical

}



use KnightMove::*; // use of globe operator

fn main() {

   // use enum

   let horizontal_move = Horizontal; // Horizontal is shortcut for KnightMove::Horizontal

   let vertical_move = Vertical; // Vertical is shortcut for KnightMove::Vertical

   // print the enum values

   println!("{:?}", horizontal_move);

   println!("{:?}", vertical_move);

}


```
output

```
Horizontal
Vertical

```

# Quiz 

{{<quizdown>}}
Test your understanding of nested modules, the use keyword and the globe operator `*`!

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---



# You can only nest the modules upto three levels.
- [ ] True 
- [ ] False 

# The followinng enum is declared
```
enum Gender {
    Male, Female
}

```
How would you use the glob operator ?
- [ ]  `use Gender :: *`
- [ ]  `Gender :: *`


# What is the output of the following code? 

```
pub mod chapter {
    pub mod lesson {
        pub fn summary(){
            println!("This is the summary"); 
        } 
        pub mod heading { 
            pub fn illustration() {  
              println!("Hi, I'm a 3rd level nested function");
            }
        }
    }
}
use chapter::lesson::heading;
use chapter::lesson;
 
fn main() {
    lesson::summary();
    heading::illustration(); 
}


```
- [ ] ```
This is the summary
Hi, I'm a 3rd level nested function
```
- [ ] ```
Hi, I'm a 3rd level nested function
```

{{</quizdown>}}
