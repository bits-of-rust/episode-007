# episode-007
Where we discover types

## Setup
The following needs to be prepared

* A project called `types`
* Some example code with a `&str` and a `i32`

## Script
We used variables to bind values to names, as seen in this code.

```rust
let message = "Hello, world!";

println!("{}", message);

let answer = 42;

println!("the answer is {}", answer);
```

But the declaration of the variables is not complete. What is missing is the *type declaration*. For example `answer` has type `i32`.

```rust
let answer: i32 = 42;
```

The reason that [Rust][rust-lang] allows you to declare a variable without explicitly mentioning the type is [type inference][type-inference]. [Rust][rust-lang] can often deduce the type of an expression, making an explicit declaration superfluous.

Sometimes we want to have more control over the type of a variable. The are numerous integer types like, for example `i8`, `i16`, `i32` and `i64`, that differ in the amount of bits that is used to represent the value.

The type can also have influence the program. If we change the value of the answer to `255` and go down the mentioned types `i64`, `i32`, `i16` until `i8`, we see that then it overflows into `-1`. Notice that [Rust][rust-lang] warns us about that behavior.

And there you have it, we discovered types.

[rust-lang]: https://www.rust-lang.org
[type-inference]: https://en.wikipedia.org/wiki/Type_inference