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




##   

