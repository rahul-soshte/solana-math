# File Specific passes of the spl-math library

## entrypoint.rs

It has the standard process_instruction function found in most native solana program which process the instructions related to the spl-math program.

## instruction.rs

Compilation of all instruction available in the Math Program
Also has utility functions which help in building a Instruction Data.
The available instructions for the program which are as follow

### 1. Integer Arithmetic

#### a. U64 Operations
- **U64Multiply**: Multiplying 2 u64 values
- **U64Divide**: Dividing 2 u64 values
- **SquareRootU64**: Calculating square root for u64 without the PreciseNumber representation

#### b. U128 Operations
- **U128Multiply**: Multiply 2 u128 values
- **U128Divide**: Divide 2 U128 values
- **SquareRootU128**: Calculating square root for u128 without the PreciseNumber representation

### 2. Floating Point Arithmetic

#### a. F32 Operations
- **F32Divide**: Dividing 2 f32 values
- **F32Exponentiate**: Calculating the power of f32 base with a f32 exponent
- **F32NaturalLog**: Logarithm of a f32 float value
- **F32NormalCDF**: Calculate the Cumulative Distribution Function of a normal distribution of F32 values

#### b. F64 Operations
- **F64Pow**: Power of a f64 base with a f64 exponent
- **F64Divide**: Divide 2 f64 values
- **F64Multiply**: Multiply 2 f64 values

### 3. Special Instructions
- **PreciseSquareRoot**: Calculates the square root for u64 type using PreciseNumber representation
- **Noop**: An empty instruction which doesn't do anything

##  error.rs

Declares 2 error types, Overflow and Underflow. Nothing much in this files besides that.

## precise_number.rs

A wrapper for U256 to do operations like power and square root and basic arithmetic support of mul, div, add and sub. No normal cdf and logarithms is implemented for it tho.

## checked_ceil_div.rs

Don't know in which use case will this be used, but this division method is more about finetuning the quotient and divisor.

## processor.rs

Standard file for any solana program.