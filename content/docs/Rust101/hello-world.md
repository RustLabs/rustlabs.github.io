---
title: Hello World
weight: 2
page: true
---

#### Getting Started with "Hello, World! "

It's universal truth everybody starts their journey with the hello world program.

create `hello.rs` file with the following content :


```rust
fn main() {
    println!("Hello World!");
}

```

*   functions are defined using fn the name of this function in main.
    
*   `println` is a micro and will print txt to STDOUT.
    
*   the body of the program is enclosed in curly braces.


rust will automatically start in the main function. function parameter appears inside the parentheses that follow the name of the function. because there is no argument lists in `main()` . the function takes no arguments.

to run this program, you must first use rust compiler, `rustc` to compile the code.

```rust
$ rustc hello.rs
```
<br>

![](/img/diagrams/1.hello-world.png)

on macOS, you can use the file command to see what kind of file this is

```bash
rustlabs file hello
hello: Mach-O 64-bit executable arm64
```

you can execute your program like this on mac

```bash
rustlabs ./hello
hello,world!
```

The dot(.) indicates the current directory and the slash(/) is the path separator. The path separator is a forward slash(/) on macOS and Linux and a backslash(\) on Windows.
you can execute your program like this if your using windows

```bash
rustlabs ./hello.exe
hello,world!
```

🍾 cheers!


## Knowledge check 


{{< quizdown >}}
---
primaryColor: steelblue
secondaryColor: '#e8e8e8'
textColor: black
shuffleQuestions: false
shuffleAnswers: true
locale: en
---

#### What is the keyword for declaring a function?

- [ ]  fun
- [ ]  function
- [ ]  func
- [x]  fn

#### What is the output of the following code?

  ```rust
    fn main() {
    println!("Hello World!")
    println!("Hello");
    }
  ```
 
  - [ ]  Hello World! \n
         Hello
  - [X] error


{{< /quizdown>}}

<br>


#### Organizing a Rust Project :

for any project, we all write multiple source files and execute them as a single binary. let's remove our existing hello binary `rm hello`

let's create a parent directory

```bash

$ mkdir -p hello/src
```

now move the `hello.rs`source file into `hello/src` using the mv command

```bash
$ mv hello 
$ rustc src/hello.rs
```

check the content of the directory using `tree` command :

```bash
➜  rustlabs tree
.
└── hello
    └── src
        └── hello.rs
```


#### What is a macro?


A macro is an expression that has
an exclamation mark (!) before the parenthesis () , i.e.,


                                 macro_name ! ( );
                                 
# What are macros used for?

They are used in metaprogramming, i.e., code that writes code. They look like functions in other system programming languages like C and C++, but instead of generating a function call like functions, they are expanded into source code that gets compiled with the rest of the program. In this way, they provide more run-time features.     


![](https://raw.githubusercontent.com/sangam14/RustLabs/master/img/metaprogram.png)

# Types of Macros

Rust provides us with some built-in macros, like the println!() above, and users can define their own macros as well.


For now, the information above will suffice, but more details on macros will be covered in the advanced track 










   

