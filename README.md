#### ERC20 test

##### 1. Substrate Prerequisites
```bash
rustup component add rust-src --toolchain nightly-2020-10-06
rustup target add wasm32-unknown-unknown --toolchain stable
rustup install nightly-2020-10-06
rustup target add wasm32-unknown-unknown --toolchain nightly-2020-10-06
```

##### 2. canvas-node
```bash
cargo +nightly-2020-10-06 install canvas-node --git https://github.com/paritytech/canvas-node.git --tag v0.1.0 --force
```

##### 3. ink! CLI

```bash
cargo install cargo-contract --vers 0.7.0 --force
```

##### 4. test and build ERC20 contract

```bash
cargo +nightly-2020-10-06 test
cargo +nightly-2020-10-06 contract build
cargo +nightly-2020-10-06 contract generate-metadata
```

##### 5. run a canvas node
```bash
canvas --dev --tmp
```

##### 6. interact by [canvas-ui](https://paritytech.github.io/canvas-ui)

The UI will connect to the locally running node by default.