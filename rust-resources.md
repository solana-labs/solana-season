# Resources for New Rust Developers

If you’re learning Rust for the first time, such as to participate in an event, here are some resources to help you ramp up.

## Introduction Material

For a quick “learn by doing” introduction to Rust code, try fasterthanlime’s worked examples for Advent of Code 2020 in Rust: [Avent of Code](https://fasterthanli.me/series/advent-of-code-2020)

You may also find this whirlwind tour of Rust syntax useful, especially for reading other Rust code you find: [A Half Hour To Learn Rust](https://fasterthanli.me/articles/a-half-hour-to-learn-rust).

fasterthanlime’s site has many other good guides to aspects of Rust, such as this guide to Box: [Whats in the Box](https://fasterthanli.me/articles/whats-in-the-box)

And this guide to string types (&str and String): [Working With Strings in Rust](https://fasterthanli.me/articles/working-with-strings-in-rust)

If you find yourself wandering through articles there for a while, you’re likely to have a productive learning adventure through both introductory and advanced topics.

The official documentation includes an example-based introduction as well, Rust By Example: [Rust By Example](https://doc.rust-lang.org/stable/rust-by-example/index.html)

As you read about Rust, you may come across many references about Rust letting you write zero-overhead zero-copy fast code. This can lead to a lot of stress when writing your own Rust code, if you’re constantly thinking about things like avoiding copies and clones, avoiding Box, avoiding Rc and Arc, and similar. Please see this Twitter thread from one of the Rust language leads for some advice about that: [Twitter Thread](https://twitter.com/josh_triplett/status/1316634750669344768)
Remember, you can always optimize your code later, once you have it working, and once profiling tells you what you actually need to optimize. This doesn’t just apply when you’re learning Rust; this applies even when you’re experienced with Rust.

## References

For a full tutorial-style introduction to much more of the language, see the official Rust book: [Official Rust Book](https://doc.rust-lang.org/stable/book/index.html)

For in-depth references, see the Rust documentation: [Rest References](https://doc.rust-lang.org/stable/)
In particular, you’ll want to have the standard library guide handy to look up APIs: [Standard Library Guide](https://doc.rust-lang.org/stable/std/index.html)
And the Cargo book for details on building Rust packages (“crates”) with Cargo: [Cargo Book](https://doc.rust-lang.org/stable/cargo/index.html)

## Other Resources

To simplify adding dependencies to your crates, run `cargo install cargo-edit`, and then use `cargo add somecrate` to add somecrate as a dependency.

Remember that your “main” function can return a Result, and if it returns an Err, Rust will automatically print that error before exiting the program with an error code. So you can bubble Results up using the `?` operator all the way to main. For a simple error type for many programs, try the `anyhow` crate. For libraries, consider the `thiserror` crate to provide an enum with distinct values for different errors.

If you’re coming from Python, and you’re interested in integrating Rust and Python, try PyO3: [PyO3](https://pyo3.rs/)

If you’re coming from C, C++, or a similar language, and you’re interested in an in-depth look at Rust, at unsafe Rust code, and at what Rust’s borrow checker and other mechanisms protect you from, try this guide: [I am a Java/C#/C/C++ Dev Learning Rust](https://fasterthanli.me/articles/i-am-a-java-csharp-c-or-cplusplus-dev-time-to-do-some-rust)

If you use DuckDuckGo, you can search the Rust documentation by adding !rust to your search (for instance, !rust Option will find the documentation for Option and its many helper methods), search the crates.io package registry by adding !cargo to your search (for instance, !cargo blake3), and look up the documentation for a specific crate with !docsrs cratename (for instance, !docsrs bstr).
