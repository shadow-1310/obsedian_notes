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
- accessing a nth character of a String 
	- we can use the str.chars().nth(N) method, but it has O(N) complexity
	- we can use str.as_bytes()[n], this is O(N) time complexity, as suggested by [this stackoverflow post](https://stackoverflow.com/questions/71824249/get-value-of-nth-char-in-string-in-rust)
	- and finally we can convert the String to vector and then access its characters 
```rust
let chars: Vec<&char> = str.chars().collect()
```
- get ordinal value (ASCII value) of a character in a vector
	- stackoverflow post https://stackoverflow.com/questions/75558423/how-do-i-convert-to-ascii-in-rust
```rust
let s = String::from("abc");
let value = s[index as usize].to_ascii_lowercase() as i32;
```
- assert_eq! with empty vector for testing purpose
	- https://stackoverflow.com/questions/63092178/how-do-i-annotate-the-type-of-an-empty-slice-in-rust
```rust
let a: Vec<String> = Vec::new();
assert_eq!(vec!["";0], a);

let b: Vec<i32> = Vec::new();
assert_eq!(vec![0;0], b);
```
## Daywise
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