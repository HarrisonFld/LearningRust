# Learning Rust

## Define a function
fn functionName {
    //function body
}

## Print a newline
println!("text"); // Calls the print newline macro

## Compile rust code
rustc code.rs
./code //Run output executable

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


