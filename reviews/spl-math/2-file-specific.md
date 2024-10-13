# File Specific Observation of the spl-math library

## entrypoint.rs

It has the standard process_instruction function found in most native solana program which process the instructions related to the spl-math program.


## instruction.rs

Compilation of all instruction available in the Math Program
Also has utility functions which help in building a Instruction Data.

The available instructions for the program which are as follow

1. PreciseSquareRoot 

It looks like it is a instruction which would help in calculating for any Unsigned integer type, but it only calculates the square root for u64 type

2. SquareRootU64 

Calculating square root for u64 without the PreciseNumber representation

3. SquareRootU128 

Calculating square root for u128 without the PreciseNumber representation

4. U64Multiply 

Multiplying 2 u64 values

5. U64Divide 

Dividing 2 u64 values

6. F32Divide 

This is floating point arithmetic, not fixed point arithmetic. Dividing 2 f32 values.

7. F32Exponentiate 

Calculating the power of f32 base with a f32 exponent.

8. F32NaturalLog  

Logarithm of a f32 float value

9. F32NormalCDF 

Calculate the Cumulative Distribution Function of a normal distribution of F32 values

10. F64Pow

Power of a f64 base with a f64 exponent

11. U128Multiply 

Multiply 2 u128 values

12. U128Divide 

Divide 2 U128 values

13. F64Divide 

Divide 2 f64 values

14. F64Multiply

Multiply 2 f64 values


15. Noop

Something like an empty instruction which doesnt do anything as such.

##  error.rs

Declares 2 error types, Overflow and Underflow. Nothing much in this files besides that.

## precise_number.rs

A wrapper for U256 to do operations like power and square root and basic arithmetic support of mul, div, add and sub. Not normal cdf as well.

## checked_ceil_div.rs

Don't know in which use case will this be used, but this division method is more about finetuning the quotient and divisor.

## approximations.rs

Useful for calculating square root, but not sure if it can be used for arithmetic calculations of large integers since it only shows usage of u128 and f32 in the unit tests.


## processor.rs

Standard file for any solana program.