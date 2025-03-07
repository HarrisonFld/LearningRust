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

## Shadowing
Variables can be shadowed. They can be overwritten during compile time, and can revert to the original value,
once the shadow scope is gone.
let name = "value"; //name = "value"
{
    let name = "new value"; //name = "new value"
}
//name = "value"

## Tuples
Group data of different data types into one variable. The size of the tuple cannot be changed.
let tup: (i32, f64, u8) = (500, 6.4, 1);
let (x, y, z) = tup;
println!("{x}"); //prints 500
let test = tup.1; //access data by index
println!("{y}"); //prints 6.4

## Arrays
Group data of the same data type in one variable. The size of the array cannot be changed.
let a = [1, 2, 3, 4, 5];
let a: [i32; 5] = [1, 2, 3, 4, 5]; //data type = i32 and amount of values = 5
let a: [2.3; 5] = [2.3, 2.3, 2.3, 2.3, 2.3] //specify each value to start at 2.3 and the amount of values = 5.
a[0]; //access value at index 0

## Functions
Functions, are reusable pieces of code that has parameters that must have their type declared. They can also
specify a return type.
fn functionName(value: type, num: i32) -> i32 { //define a function with 2 parameters that returns a i32 value
    //function body
    println!("{value} and {num");
}

