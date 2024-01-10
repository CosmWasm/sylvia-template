# `sylvia-template`

This is a project template for use with the [_Sylvia framework_](https://github.com/CosmWasm/sylvia).

## Generating a project scaffold

### Prerequisites

You need `cargo-generate` installed on your system.

```sh
cargo install cargo-generate
```

### Usage

```sh
cargo generate CosmWasm/sylvia-template
```

Or, to provide the name of the project non-interactively:

```sh
cargo generate CosmWasm/sylvia-template -n my-contract
```

## License

The template itself is [licensed under the Apache 2.0 license](LICENSE). After generating, no license file is included with your new project - you might want to add one if you're making your source code publically available!
