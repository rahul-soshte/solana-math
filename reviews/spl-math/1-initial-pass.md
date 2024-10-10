# Initial Pass of the spl-math library

(The link to the spl-math library)
[https://github.com/solana-labs/solana-program-library/tree/master/libraries/math]

(The link to the docs.rs)[https://docs.rs/spl-math/latest/spl_math/]

## Reference Commit

https://github.com/solana-labs/solana-program-library/commit/cd6ce4b7709d2420bca60b4656bbd3d15d2e1485


## Observations

1. It uses the ```uint``` crate from parity's (codebase)[https://github.com/paritytech/parity-common/tree/master/uint]

2. It is a onchain math program and not a standalone library. So need to CPI call to do some arithmetic operation.

3. The following distinct files which define the business logic of the math lib

-> approximation.rs
-> checked_ceil_div.rs
-> entrypoint.rs 
-> error.rs
-> instruction.rs
-> precise_number.rs

4. Need to dig deep into each file, to review the business logic and the algorithms used for the each arithmetic operations.