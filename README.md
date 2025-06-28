# Rust from zero to production

## Start

```shell
# Install the following crate.
cargo install cargo-watch

# Monitor like this.
cargo watch -x check

# Or even chain different commands.
cargo watch -x check -x test -x run
```

- Create the `.cargo/config.toml` file for the `cargo watch` command.


```shell
# Additional components required to compute LLVM code coverage.
rustup component add llvm-tools-preview
cargo install cargo-llvm-cov

# Run it to show tests.
cargo llvm-cov

# For more instructions.
llvm-cov --help

# For linting.
rustup component add clippy
cargo clippy
# To check if clippy emits any warnings.
cargo clippy -- -D warnings

# For formatting.
rustup component add rustfmt
# To format the whole project.
cargo fmt
# For the CI pipeline.
cargo fmt -- --check

# For security vulnerabilities
cargo install cargo-audit
# Run it.
cargo audit
```

Use the following to setup [GitHub Actions](https://github.com/LukeMathWalker/zero-to-production/tree/root-chapter-03-part0/.github/workflows)
