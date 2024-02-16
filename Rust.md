### Learning Resources
- [medium article - original](https://towardsdatascience.com/python-to-rust-breaking-down-3-big-obstacles-094eb99e331d)
	- [medium article - archived](https://archive.is/hjNHh)

[The Book](https://doc.rust-lang.org/book/)
```bash
rustup docs --book
```

[rustlings-github repo](https://github.com/rust-lang/rustlings/)
```bash
rustlings watch
```
[Rust by example](https://doc.rust-lang.org/rust-by-example/)
[Rust by practice](https://practice.rs/why-exercise.html)
```bash
mdbook serve en/
```

PyO3 to call Rust from Python

### Learnings
---
#### Day1 - [[2024-01-06]]
- learnt shadowing
	- for unused variable compiler will through error
- error handling
	- expect
- Always trim values when taking inputs from user as it contains '\n'
- statements and expressions
	- statements does not have return value
	- expression have return value
	- at then last line of a block, don't add ';'
- functions
	-  In Rust, the return value of the function is synonymous with the value of the final expression in the block of the body of a function.
- Loops
	- we can give name to loops

#### Day2 - [[2024-01-07]]
- Ownership and borrowing
	- String and String literals
		- String can be mutable and are of variable size
		- string literal is immutable and hardcoded at compile time
			- they are also fixed size