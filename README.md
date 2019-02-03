# SubstrateKitties Learning

>  Following along the [Substrate collectables workshop](https://github.com/shawntabrizi/substrate-collectables-workshop) for learning about [Substrate](https://github.com/paritytech/substrate).

### Instructions and notes

### runtime

Installing Substrate after Rust is installed:

```bash
curl https://getsubstrate.io -sSf | bash
source ~/.cargo/env
```

Creating new parachain node from a template:

```bash
substrate-node-new substratekitties <author-name>
```

Building WASM runtime:

```bash
cd substratekitties
./build.sh
```

Building binary and running:

```bash
cargo build --release
./target/release/substratekitties --dev
```

Simply running after building WASM runtime:

```bash
cargo run -- --dev
```

Purging chain data (required after modifying runtime):

```bash
cargo run -- purge-chain --dev
```

UI for interacting with methods and storage:

[https://polkadot.js.org/apps/](https://polkadot.js.org/apps/)

### Frontend

Create new frontend project from boilerplate:

```bash
substrate-ui-new substratekitties
```

Install dependencies:

```bash
cd substratekitties-ui/
yarn install
```

Start app:

```bash
yarn run dev
```

Recover seed for import:

```bash
subkey restore Alice
```

# License

[MIT](LICENSE)