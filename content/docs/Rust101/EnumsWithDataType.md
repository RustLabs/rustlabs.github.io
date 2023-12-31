---
title: Enums With Data Type
weight: 58
---

# Enums With Data Type

By default, the Rust compiler infers the data type for all variants of an enum. However, 
it is possible to use different data types for different variants of an enum.

# Syntax 
- The data type can be added to each variant enclosed within round brackets `()`.

![](/img/diagrams/102.enum-data-type.png)

- Example 
The following example makes an enum KnightMove having two variants Horizontal and Vertical both of type String.

```
// make this `enum` printable with `fmt::Debug`.

#[derive(Debug)]

enum KnightMove{

   Horizontal(String), Vertical(String)

}

fn main() {

   // invoke an enum

   let horizontal_move = KnightMove::Horizontal("Left".to_string());

   let vertical_move = KnightMove::Vertical("Down".to_string());

   // print enum

   println!("Move 1: {:?}", horizontal_move);

   println!("Movw 2: {:?}", vertical_move);

}

```

output 

```
Move 1: Horizontal("Left")
Movw 2: Vertical("Down")

```



