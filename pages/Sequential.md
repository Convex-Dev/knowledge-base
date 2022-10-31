filters:: {"vector" false, "collection" false}
---

- Property of a [[Collection]] ordering its [[Values]] sequentially
- Under an expected order guaranteed to remain stable
- Each [[Value]] can be referred to by its position
	- Starting at `0`
	- Access beyond the capacity of the [[Vector]] results in a [[:BOUNDS]] error
- ---
- A [[Sequential]] [[Collection]] is always [[Associative]]
- ---
- See
	- [[List]]
	- [[Vector]]