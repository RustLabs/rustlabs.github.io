---
title: Tuples
weight: 13
---

# What are Tuples? 

- Tuples are heterogeneous sequences of elements, meaning, each element in a tuple can have a different data type. Just like arrays, tuples are of a fixed length.

![](/img/diagrams/20.tuple.png)


- Define a Tuple 

A tuple can be defined by writing let followed by the name of the tuple and then enclosing the values within the parenthesis.

- Syntax 1 
   - The syntax below defines a tuple without specifying the type. However, the compiler can infer the type.
   
![](/img/diagrams/21.tuple-syntax1.png)

 - Syntax 2
     - The syntax below defines a tuple by specifying the type.

![](/img/diagrams/22.tuple-syntax2.png)    
 
 # Example 

The following illustration explains the concept:

```rust

#[allow(unused_variables, unused_mut)]
fn main() {
    //define a tuple
    let person_data = ("Alex", 48, "35kg", "6ft");
    // define a tuple with type annotated
    let person_data : (&str, i32, &str, &str) = ("Alex", 48, "35kg", "6ft");
}

```

- Access the Value of the Tuple 
- Unlike array which uses `[]` for accessing an element, the value of the tuple can be accessed using the dot operator ` (.) `.
 
 ```
 tuplename.indexvalue
 
 ```
 To get the individual values out of a tuple, we can use pattern matching to destructure a tuple value, like this:
 
 ```
 let person_data = ("Alex", 48, "35kg", "6ft");
    let (w, x, y, z) = person_data;
 
 ```
 
 ```
 fn main() {
    //define a tuple
    let person_data = ("Alex", 48, "35kg", "6ft");
    // access value of a tuple
    println!("The value of the tuple at index 0 and index 1 are {} {}",person_data.0,person_data.1);

    //define a tuple
    let person_data = ("Alex", 48, "35kg", "6ft");
    // get individual values out of tuple
    let (w ,x, y, z) = person_data;
    //print values
    println!("Name : {}",w);
    println!("Age : {}",x);
    println!("Weight : {}",y);
    println!("Height : {}",z);
}
 

```
 output:- 
 
```
 The value of the tuple at index 0 and index 1 are Alex 48
Name : Alex
Age : 48
Weight : 35kg
Height : 6ft
 
```
 
# How to Make a Tuple Mutable? 

Just like a variable becomes mutable by adding the mut keyword after let, the same goes for a tuple.

```
fn main() {
    //define a tuple
    let mut person_data = ("Alex", 48, "35kg", "6ft");
    //print the value of tuple
    println!("The value of the tuple at index 0 and index 1 are {} {}", person_data.0, person_data.1);
    //modify the value at index 0
    person_data.0 = "John";
    //print the modified value
    println!("The value of the tuple at index 0 and index 1 are {} {}", person_data.0, person_data.1);
}

```
output:- 

```
The value of the tuple at index 0 and index 1 are Alex 48
The value of the tuple at index 0 and index 1 are John 48
```

# Print the Tuple 

The whole tuple can be traversed using the debug trait.

```
fn main() {
    //define a tuple
    let person_data = ("Alex", 48, "35kg", "6ft");
    //print the value of tuple
    println!("Tuple - Person Data : {:?}",person_data);
}


```
output:- 

```
Tuple - Person Data : ("Alex", 48, "35kg", "6ft")



```
# Quiz 

Test your understanding of tuples in Rust!

{{<quizdown>}}

---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---




# Which of the following statements is not true? 
- [ ] Tuple is immutable by default 
- [ ] Array is immutable by default 
- [ ] Tuple can never be made mutable 
- [ ] Array can never be made mutable 

# What is the output of the following code snippet? 

```rust
let (w ,x, y, z) = ("1","3","2","4");
println!("w : {}",w);
println!("x : {}",x);
println!("y : {}",y);
println!("z : {}",z);
```

- [ ]  ```
w : 1
x : 3
y : 2
z : 4
```    

- [ ] ```
w : 1
x : 2
y : 3
z : 4
```

{{</quizdown>}}