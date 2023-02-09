# Comparison building on Plonky2 vs Halo2

Our aim is to implement these spefication circuits in Plonky2. However many zk projects in are currently built on Halo2, so they are a good basis for learning. 

This document is a stub, and intended to document how we can build custom gates and gadgets in Plonky2. Careful, we might be wrong on all accounts and this document should be treated with care.

## Halo2 vs Plonky2

Halo2 is a modern proof system with good adoption and support. It is transparant, based on PLONK arithmetization (PLONKish), and is able to achieve recursion through cycles of elliptic curves. It is well documented and supported by the ZCash team, for reference see [The Halo2 handbook](https://zcash.github.io/halo2/index.html).
However, while recursion is meaningfully possible with Halo2, it still requires deep insight into the underlying mathematics for building and aggregating proofs.

Plonky2, is built by Polygon Zero, previously Mir Protocol, and makes ostensibly good engineering decisions: it combines PLONK based arithmetization[^Plonkish], with FRI as a proving backend. As a they can use the Goldilock field as a finite field, which has good performance on existing 64-bit hardware. Additionally, thanks to FRI, they can achieve recursion with this single field, promising to simply the design of composite proof systems. [Plonky2](https://github.com/mir-protocol/plonky2) is younger and not yet officially released, but actively developed and backed by a strong team.

[^Plonkish]: todo: both Plonky2 and Halo2 are PLONKish in that they support custom gates and lookup arguments, but to what extend are specifications implementable in either?
