---
title: Hello World
weight: 2
icon: "👋"
page: true
---

{{% alert icon="⌨️" context="success" %}}
Setting up a Rust development environment involves several steps. Here's a pre-request list to get you started:

1. **Install Rust:**
Use rustup, the Rust toolchain installer. It manages Rust versions and associated tools for you.
2. **Configure Your Environment:**
Ensure that the Rust installation is added to your system's PATH.
Set up your preferred text editor or IDE with Rust support. Popular choices include Visual Studio Code, IntelliJ IDEA, and others with Rust plugins or extensions.
3. **Install Essential Tools:**
cargo: Rust's package manager and build system, typically installed with Rust.
rustfmt: A tool for formatting Rust code according to style guidelines.
clippy: A collection of lints to catch common mistakes and improve your Rust code.
4. **Clone The Repo** 
```
gh repo clone RustLabs/RustLabs-Workshop
```

 <a href="https://github.com/RustLabs/RustLabs-Workshop"><img src="https://github-link-card.s3.ap-northeast-1.amazonaws.com/RustLabs/RustLabs-Workshop.png" width="460px"></a>

🌟 star the repo for supporting 🙏

{{% /alert %}}


### Getting Started with "Hello, World! "

It's universal truth everybody starts their journey with the hello world program.

create ***hello.rs*** file with the following content :


<!-- code snippet -->
<pre>fn main() {
    println!("Hello World!");
}</pre>

<!-- playground widget attaches to the previous snippet -->
<codapi-snippet sandbox="rust" editor="basic">
</codapi-snippet>

<!-- playground script -->
<script src="https://unpkg.com/@antonz/codapi/dist/snippet.js">
</script>


* In Rust, functions are declared using the fn keyword followed by the function's name. For instance, the main function is the entry point of a Rust program.

* println! is a macro, not a function, and is used for printing text to the standard output (STDOUT). The exclamation mark distinguishes it as a macro.
The program's code, including the main function, is enclosed within curly braces {}.

* In Rust, execution begins with the main function. If a function has parameters, they are specified within parentheses () after the function's name. The main function in the standard format, with () and no parameters, indicates that it does not accept any arguments.

* To execute a Rust program, you need to compile it first. This is done using the Rust compiler, rustc. After compilation, an executable is generated which can be run to execute the program

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


### Organizing a Rust Project :

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


``` macro_name ! ( );```
                                 
### What are macros used for?

Macros in Rust are powerful tools for metaprogramming, which involves writing code that generates other code. Unlike functions in languages such as C or C++, macros don't result in function calls. Instead, they expand into source code that is then compiled along with the rest of the program. This approach allows for additional runtime capabilitie     


![](/img/metaprogram.png)

### Types of Macros

An example of a built-in macro in Rust is ```println!```, which is used for printing output. Rust also allows users to define their own custom macros.


While this overview provides a basic understanding of macros, more in-depth information on this topic is available in advanced Rust programming resources.










   

