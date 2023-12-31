---
title: Slicing a Vector
weight: 51
---

# Slicing a Vector

- Get Slice 
Imagine a situation where you need to get a portion of a vector. Rust allows you to borrow the slice of the vector instead of using the whole vector.

- Syntax 
Slice is a two-word object. The first word is a pointer to the data, and the second word is the length of the slice.



```
fn main() {
   // define a vector of size 5
   let my_vec = vec![1, 2, 3, 4, 5];
   let slice:&[i32] = &my_vec[2..4];
   // print the vector
   println!("Slice of the vector : {:?}",slice);
}

```
output 

```
Slice of the vector : [3, 4]

```

# Quiz 

Test your understanding of vector array slicing in Rust! <br>

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
   let my_vec = vec![1, 2, 3, 4, 5];
   let slice:&[i32] = &my_vec[2..6];
   println!("Slice of the vector : {:?}",slice);
}

```
- [ ] ```
    Slice of the vector : [3, 4, 5] 
   ```
- [ ] Run time error  


# What is the output of the following code? <br>

```
fn main() {
   let my_vec = vec![2, 3, 9, 8,7];
   let slice:&[i32] = &my_vec[2..4];
   println!("Slice of the vector : {:?}", slice);
}

```

- [ ] Slice of the vector : [3, 9]

- [ ] Slice of the vector : [9, 8]


{{</quizdown>}}





