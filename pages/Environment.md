- An Environment on the CVM is a mapping from Symbols to defined values.
- The Convex environment should be familiar to those who study the formal semantics of programming languages. It is implemented as a functional, immutable map, where new definitions result in the creation and usage of a new Environment.
- Each Account receives it's own independent Environment for programmatic usage. If the Account is an Actor, exported definitions in the environment define the behavior of the Actor.