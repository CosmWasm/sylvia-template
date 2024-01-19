# `sylvia-template`

This project template is designed for the [_Sylvia framework_], a comprehensive tool for building CosmWasm smart contracts.(https://github.com/CosmWasm/sylvia).

## Generating a project scaffold

## Prerequisites

Before you begin, ensure `cargo-generate` is installed on your system.

```sh
cargo install cargo-generate
```

## Usage

Generate a new project using:

```sh
cargo generate CosmWasm/sylvia-template
```

Alternatively, specify your project's name directly:

```sh
cargo generate CosmWasm/sylvia-template -n my-contract
```


## Developer's guide

The Sylvia framework aims to minimize boilerplate code in contract development. By utilizing a few procedural macros, it allows developers to concentrate on the core business logic of the contract. The [Sylvia book](https://cosmwasm.github.io/sylvia-book/) is an excellent resource for getting started.

This template repository includes a sample contract and scripts to assist in the development process.

## Cargo scripts

Cargo scripts can be run without any additional tools other than the cargo itself. They are a useful aliases for the more complex commands:
 * `cargo wasm` - compiles the Wasm release binary,
 * `cargo wasm-debug` - compiles the Wasm debug binary, useful for testing,
 * `cargo schema` - generates JSON schema of the contract's messages.


## Validating the Webassembly binary

Post-compilation, validate the Webassembly binary's integrity using [cosmwasm-check](https://crates.io/crates/cosmwasm-check). A user guide is available on the  [crates.io](crates.io) repository.


## Using contract as a dependency to another contract

Sylvia-built contracts can also be integrated as dependencies in other contracts. The `library` feature flag in this repository omits entry point generation, allowing the contract to function as a dependency. Activating this feature  prevents entry point collisions when using the contract in another crate. More details are in the Sylvia Book.

## Testing

Syvlia supports multiple testing methods, including unit tests and multitests, without a blockchain testing environment. Examples of both are provided in this template.


## License

The template itself is [licensed under the Apache 2.0 license](LICENSE). After generating, no license file is included with your new project - you might want to add one if you're making your source code publically available!
