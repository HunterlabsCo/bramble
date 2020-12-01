## What is Bramble?
Bramble is a PoS blockchain meant to create a universal reward ecosystem for games, social media and online applications. It is uses the Substrate Framework as a base.
It uses the Grandpa Finality Gadget and Babe Block Production Mechanism together to create a consensus.

## Prerequisites
1) Rust (https://www.rust-lang.org/tools/install)

## How to run a local development chain
```
cargo run -p node-cli --release -- --dev --tmp
```

## How to run Alice and Bob Local Testnet
To remove old Alice and Bob RocksDB:

```
cargo run -p node-cli --release -- purge-chain --base-path /tmp/alice --chain local 
cargo run -p node-cli --release -- purge-chain --base-path /tmp/bob --chain local 
```

To start Alice Node
```
cargo run -p node-cli --release -- --base-path /tmp/alice --chain local --alice --port 30333 --ws-port 9945 --rpc-port 9933 --node-key 0000000000000000000000000000000000000000000000000000000000000001 --validator

```

To Start Bob Node
```
cargo run -p node-cli --release -- --base-path /tmp/bob --chain local --bob --port 30334 --ws-port 9946 --rpc-port 9934 --validator --bootnodes /ip4/127.0.0.1/tcp/30333/p2p/12D3KooWEyoppNCUx8Yx66oV9fJnriXwCcXwDDUA2kj6vnc6iDEp

```

## Cartman Testnet
It is a work-in-progress. If you want to contribute read more about https://substrate.dev/

## Contact and Discord Channel

Email: hunterlabsc@gmail.com<br/>
Discord: https://discord.gg/jeqAnF4Tuy
