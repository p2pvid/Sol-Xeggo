# 🏗 Sol-Xeggo
Recurring Platform built on Solana

Video Link: https://drive.google.com/file/d/1nbYFvBJho-fQLhWyppIuXEo-lvgzCmcw/view?usp=sharing

PPT: https://docs.google.com/presentation/d/1wZO9C7R0p7zESB4R2ZaX4MXgCo3D0XGrZ4H5gC1A1Ac/edit?usp=sharing

# Quickstart

```bash
git clone https://github.com/solana-labs/dapp-scaffold.git

cd dapp-scaffold
```

```bash

yarn

```

```bash

yarn start

```

# Environment Setup
1. Install Rust from https://rustup.rs/
2. Install Solana v1.6.7 or later from https://docs.solana.com/cli/install-solana-cli-tools#use-solanas-install-tool
3. Install Node
4. Install NPM, Yarn

# Build Smart Contract (compiled for BPF)
Run the following from the program/ subdirectory:

```bash
$ cargo build-bpf
$ cargo test-bpf
```
# Directory structure

## program

Solana program template in Rust

### program/src/lib.rs
* process_instruction function is used to run all calls issued to the smart contract

## src/actions

Setup here actions that will interact with Solana programs using sendTransaction function

## src/contexts

React context objects that are used propagate state of accounts across the application

## src/hooks

Generic react hooks to interact with token program:
* useUserBalance - query for balance of any user token by mint, returns:
    - balance
    - balanceLamports
    - balanceInUSD
* useUserTotalBalance - aggregates user balance across all token accounts and returns value in USD
    - balanceInUSD
* useAccountByMint
* useTokenName
* useUserAccounts

## src/views

* home - main page for your app
* faucet - airdrops SOL on Testnet and Devnet
