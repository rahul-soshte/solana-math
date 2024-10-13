# Observations

1. It looks like a onchain program rather than a standalone library. So one needs to cross program contract call from their solana prorgam to do a arithmetic program, which feels weird, since it make more sense to do a standalone library which can be easily used in a program as a dependency. Though some parts of this spl-math can directly be copied into a developer's codebase so they can use without doing the cross program invocation

2. The PreciseNumber doesn't have logarithms and normal cdf functionality implemented.

3. Logarithms and Normal CDF are also not implemented for smaller integer types like u64, or u128.

