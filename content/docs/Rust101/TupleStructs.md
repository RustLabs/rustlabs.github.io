---
title: Tuple Structs
weight: 56
---



# Tuple Structs

What Are Tuple Structs? 
- Tuple Structs are a data type that is a hybrid between a tuple and a struct.

![](/img/diagrams/95.tuple-struct-ex1.png)


Why a tuple struct?

In the example above, when it is only a tuple we don’t know explicitly what each item in the tuple means. But when it is a tuple struct, we can assign a
name to each item.

 # Define a Tuple Struct 
- Tuples can be of type struct by adding the struct keyword before the tuple name, followed by the data type of the variables enclosed within round brackets.

![](/img/diagrams/96.tuple-struct-syntax.png)

# Initialize a Tuple Struct 
A tuple struct can be initialized like a tuple.

![](/img/diagrams/97.tuple-struct-init.png)

# Access a Tuple Struct 
The tuple struct can be accessed using a `.` operator like a traditional struct.

![](/img/diagrams/98.tuple-struct-access.png)

# Example
The following example declares a tuple struct named FruitQuantity.
```
//define a tuple struct
struct FruitQuantity(String, i32);
// main function
fn main() {
    // create an instance
    let r1 = FruitQuantity("oranges".to_string(), 12);
    // access values of a tuple struct
    println!("r1--name:{} quantity:{}", r1.0, r1.1);
    // create an instance
    let r2 = FruitQuantity("mangoes".to_string(), 13);
    // access values of a tuple struct
    println!("r2--name:{} quantity:{}", r2.0, r2.1);   
}


```

output

```
r1--name:oranges quantity:12
r2--name:mangoes quantity:13

```


main.rs 
```
#[allow(unused_variables, unused_mut)]
use std::fs::File;
use std::io::{BufRead, BufReader};
 
fn main() {
   let filename = "sublist_input.txt";
   // Open the file in read-only mode (ignoring errors).
   let file = File::open(filename).unwrap();
   let reader = BufReader::new(file);
   let mut vec1 = vec![];
   let mut vec2 = vec![];
   // Read the file line by line using the lines() iterator from std::io::BufRead.
   for (index, line) in reader.lines().enumerate() {
       let line = line.unwrap(); // Ignore errors.
       // Show the line and its number.
       println!("{}", line.to_string());
       let mystr = line.to_string();
       let bar: Vec<&str> = mystr.split(", ").collect();
       let baz = bar.iter().map(|x| x.parse::<i64>());

       for x in baz {
           match x {
               Ok(i) => if index % 2 == 0 {vec1.push(i)} else {vec2.push(i)},
               Err(_) => println!("parse failed {:?}", x),
           }
       }
       if index % 2 == 1{
        println!("vec 1{:?}", vec1);  
        println!("vec 2{:?}", vec2);   
   
        println!("{}", Comparison::Superlist == sublist(&vec1, &vec1));
        println!("{}", Comparison::Equal == sublist(&vec1, &vec1));
        println!("{}", Comparison::Superlist == sublist(&vec2, &vec1));
        println!("{}", Comparison::Sublist == sublist(&vec1, &vec2));
        println!("{}", Comparison::Unequal == sublist(&[1, 2, 1, 2, 3], &[1, 2, 3, 1, 2, 3, 2, 3, 2, 1]));
       }

}
}


#[derive(Debug, PartialEq, Eq)]
enum Comparison {
    Equal,
    Sublist,
    Superlist,
    Unequal,
}


fn sublist(a : &[i64], b : &[i64]) -> Comparison {
    if a == b {
        Comparison::Equal
    } else if contains(a, b) {
        Comparison::Superlist
    } else if contains(b, a) {
        Comparison::Sublist
    } else {
        Comparison::Unequal
    }
}

fn contains(a: &[i64], b: &[i64]) -> bool {
    if a.len() < b.len() {
        return false;
    }

    if a.starts_with(b) {
        return true;
    }

    contains(&a[1..], b)
}




```
sublist_input.txt

```
3, 4, 5
1, 2, 3, 4, 5


```
output 

```
3, 4, 5
1, 2, 3, 4, 5
vec 1[3, 4, 5]
vec 2[1, 2, 3, 4, 5]
false
true
true
true
true



```

