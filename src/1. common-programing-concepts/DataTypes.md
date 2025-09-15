# Data Types
Every value in Rust is of a certain data type, which tells Rust what kind of data is being specified so it knows how to work with data. We'll look at two data type subsets: **Scalar** and **Compound** 


## Scalar Types

A scalar type represents a single value. Rust has four primary scalar types: **integers, floating-point, numbers, Booleans, and characters.

### Integer Types
An integer is a number without a fractional component. We can use a any of these variants to declare the type of an integer value.

    Length	                Signed  Unsigned
    8-bit	                i8      u8
    16-bit	                i16     u16
    32-bit	                i32     u32
    64-bit	                i64     u64
    128-bit     	        i128	u128
    architecture dependent	isize	usize

    Signed: only positive values 0 ... n
    Unsigned: positive and negative values

We can write integer literals in any of the forms shown in teh next Table

    Number literals     Example
    Decimal             98_222
    Hex                 0xff
    Octal               0o77
    Binary              0b1111_0000
    Byte(u8 only)	    b'A'


### Floating-Point Types
Rust also has two types for floating-points numbers which are numbers with decimal points. Rust's floating types are **f32** and **f64**, wich are 32 bits and 64 bits in size, respectively. ths default type is **f64** because on modern CPUs, it's roughly the same speed as **f32** but is capable of more precision.

    fn main() {
        let x = 2.0; // f64
    
        let y: f32 = 3.0; // f32
    }

### Numeric Operations
Rust supports the basic numeric operations you'd expect for all the numbers types: addition, substraction,  multiplication, division and remainder (residuo). integer division truncates toward zero to the nearest integer.

    fn main() {
        // addition
        let sum = 5 + 10;
    
        // subtraction
        let difference = 95.5 - 4.3;
    
        // multiplication
        let product = 4 * 30;
    
        // division
        let quotient = 56.7 / 32.2;
        let truncated = -5 / 3; // Results in -1
    
        // remainder
        let remainder = 43 % 5;
    }

### Boolean Type
As in most of the programing languages, a Boolean type in Rust has two possible values: **true** and **false**. Booleans are one byte in size. the Boolean type in rust is specified using bool.

    fn main() {
        let t = true;
    
        let f: bool = false; // with explicit type annotation
    }