# Rust + Sway integration testing

A cargo-generate template that makes it easy to initialise Rust integration
testing within an existing Sway project.

This template is designed for Rust developers who wish to test integration of
their Rust application and Sway code.

## Usage

With [Rust installed][rust-installation]:

1. Install the `cargo generate` command.
   ```
   cargo install cargo-generate
   ```
   You can learn more about cargo generate by visiting [its
   repository][cargo-generate-repo].

2. Change into the directory of your existing `forc` project.
   ```
   cd /path/to/my/forc/project
   ```
   Make sure you have run `forc build` within your project at least once so that
   the output artifacts are available to the integration tests. *Note: This may
   no longer be required in the future as we hope to enable the integration
   testing to automatically build the artifacts as necessary so that they are
   always up to date!*

3. Generate your integration tests.
   ```
   cargo generate --init https://github.com/fuellabs/sway-test-rs
   ```
   The cargo generate command will prompt you for your project's name. Make sure
   the name matches your existing `forc` project name!

4. Done! Your test harness should be generated. You can run it as you would
   normal Rust tests:
   ```
   cargo test
   ```
   If all went well the initial test harness should build and run successfully!

## Useful Links:

- The Sway & Forc repository: https://github.com/fuellabs/sway
- The Fuel Rust SDK repository: https://github.com/fuellabs/fuels-rs
- The Fuel Rust SDK Book: https://fuellabs.github.io/fuels-rs/latest

[rust-installation]: https://www.rust-lang.org/tools/install
[cargo-generate-repo]: https://github.com/cargo-generate/cargo-generate
