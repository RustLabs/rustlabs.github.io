---
title: Nested Loops
weight: 33
---

# Nested Loops

- What Is a Nested Loop? 
A nested loop is a loop within a loop.
- Syntax 
Here, a for loop nested inside a for loop. However, any loop can be nested inside any loop. The general syntax is:

![](/img/diagrams/64.nested_loop.png)

# Example 

The following code prints a multiplication table of 1-5 using a nested for loop.

```
fn main() {
 for i in 1..5{ //outer loop
  println!("Multiplication Table of : {}", i);
   for j in 1..5 { // inner loop
       println!("{} * {} = {}", i, j, i * j);
   }
 }
}

```
output

```
Multiplication Table of : 1
1 * 1 = 1
1 * 2 = 2
1 * 3 = 3
1 * 4 = 4
Multiplication Table of : 2
2 * 1 = 2
2 * 2 = 4
2 * 3 = 6
2 * 4 = 8
Multiplication Table of : 3
3 * 1 = 3
3 * 2 = 6
3 * 3 = 9
3 * 4 = 12
Multiplication Table of : 4
4 * 1 = 4
4 * 2 = 8
4 * 3 = 12
4 * 4 = 16


```

# Explanation 

- Outer for Loop
   -  A for loop is defined on line 2
   -  The loop takes i as an iterator that iterates over values from 1 to 5.

- Inner for Loop

   -  A for loop is defined on line 4
   -  The loop takes j as an iterator that iterates over values from 1 to 5.
   -  For each iteration of the outer loop, the inner loop runs four times while printing the product of variables i and j.
   
 

| i 	| j 	| output 	|
|-	|-	|-	|
| <br><br>1 	|  1<br> 2<br> 3<br> 4 	| <br>1 * 1 = 1<br>1 * 2 = 2<br>1 * 3 = 3<br>1 * 4 = 4<br>  	|
| 2 	|  1<br> 2<br> 3<br> 4 	| 2 * 1 = 2<br>2 * 2 = 4<br>2 * 3 = 6<br>2 * 4 = 8 	|
| 3 	|  1<br> 2<br> 3<br> 4 	| 3 * 1 = 3<br>3 * 2 = 6<br>3 * 3 = 9<br>3 * 4 = 12 	|
| 4 	|  1<br> 2<br> 3<br> 4 	| 4 * 1 = 4<br>4 * 2 = 8<br>4 * 3 = 12<br>4 * 4 = 16 	|


Sometimes, you might need to break the outer loop instead of the inner loop. So how can you specify which loop you are referring to? You can use a loop label.

