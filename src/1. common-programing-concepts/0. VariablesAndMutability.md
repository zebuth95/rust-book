# Variables and Mutability

    fn main() {
        let x = 5;
        println!("The value of x is: {x}");
        x = 6;
        println!("The value of x is: {x}");
    }

You should receive an error message regarding an immutability error, as shown in this output:

    $ cargo run
    Compiling variables v0.1.0 (file:///projects/variables)
    error[E0384]: cannot assign twice to immutable variable `x`
    --> src/main.rs:4:5
    |
    2 |     let x = 5;
    |         - first assignment to `x`
    3 |     println!("The value of x is: {x}");
    4 |     x = 6;
    |     ^^^^^ cannot assign twice to immutable variable
    |
    help: consider making this binding mutable
    |
    2 |     let mut x = 5;
    |         +++
    
    For more information about this error, try `rustc --explain E0384`.
    error: could not compile `variables` (bin "variables") due to 1 previous error

This example shows how the compiler helps you find errors in your programs. Compiler errors can be frustrating, but really they only mean your program isn’t safely doing what you want it to do yet; they do not mean that you’re not a good programmer! Experienced Rustaceans still get compiler errors.

You received the error message cannot assign twice to immutable variable `x` because you tried to assign a second value to the immutable x variable.


    fn main() {
        let mut x = 5;
        println!("The value of x is: {x}");
        x = 6;
        println!("The value of x is: {x}");
    }
When we run the program now, we get this:

    $ cargo run
    Compiling variables v0.1.0 (file:///projects/variables)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.30s
    Running `target/debug/variables`
    The value of x is: 5
    The value of x is: 6

# Constants
Like immutable variables, constats are values that are bound to a name are not allowed to changes. Can not use mut with constants. Constants aren't mutable.

    const THREE_HOURS_IN_SECONDS: u32 = 60 * 60 * 3;

# Shadowing
You can declare a new variable with the **same name** as a previous variable. Rustaceans say that the first value is shadowed by the second, which means that the second variable is what the compiler will see when you use the named of the variable.

    fn main() {
        let x = 5;
        
            let x = x + 1;
        
            {
                let x = x * 2;
                println!("The value of x in the inner scope is: {x}");
            }
        
            println!("The value of x is: {x}");
    }

    $ cargo run
    Compiling variables v0.1.0 (file:///projects/variables)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.31s
    Running `target/debug/variables`
    The value of x in the inner scope is: 12
    The value of x is: 6

Shadowing is different from marking a variable as mut because we’ll get a compile-time error if we accidentally try to reassign to this variable without using the let keyword. By using let, we can perform a few transformations on a value but have the variable be immutable after those transformations have been completed.

