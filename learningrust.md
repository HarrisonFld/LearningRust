# Learning Rust

# Cargo -- Rust's build and package manager
cargo --version //check the executable version

## Create a new rust project
cargo new projectname

## Edit the Cargo toml
// Defines the project settings: build dependencies, version, etc.
nano Cargo.toml

## Build a rust project
cargo build

## Build and run a rust project
cargo run

## Check if rust project can compile
cargo check

## Compile and Build for release
cargo build --release //introduce rust optimizations

# Programming

## Define a function
fn functionName {
    //function body
}

## Print a newline
println!("text"); // Calls the print newline macro

## Compile rust code
rustc code.rs
./code //Run output executable

## Standard Library and Prelude
Rust comes with a standard library available for use, that brings in many common elements. In that 
standard library, it has a module, that is brought in automatically, known as a set called **prelude**.
* std::prelude
    - std::default
    - std::clone
    - std::cmp //comparisons

## Variables
let variableName = value; //define an immutable variable with an value
let mut variableName = value; //define an mutable variable with an value

## References
A reference is a pointer or a variable that stores an address to the body of the data, or a variable's
value, is stored.

Rust references are called with an &:
let string = String::new();
println!(&string); //Call println and pass in a reference to the variable string

Rust references are also immutable by default:
fakeFunction(&mut string) //Call a function with a mutable reference

## Strings
let mut stringName = String::new(); //Create an empty string

## Use
use library::tree::scope //import a library and a module 

## IO
use std::io //import or use the std io library
io::stdin() //read input
io::stdout() //write output

## Annotate Type
let variableName: type; //set a variable to infer that type
let num: u32; //u32 is a default integer type

## Match Keyword
Similar to switch statement in other languages. Compares one value to a defined set
of comparisons, and does the resulting operation if they match.
let string_var = "String";
match string_var == "String" {
    true => println!("Was a string!"),
    false => println!("Wasnt"),
}

## Loop Infinitely
loop {
    //loop body
}