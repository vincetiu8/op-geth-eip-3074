# Geth Setup
## Installation
1. Install go, c, other deps
2. Run `make all`

This will build geth and other modules into the `./build/bin` folder to use.

## Setting up the cluster
1. Run `make account`
2. Paste the account address into the alloc field in `data/pn_genesis.json`
3. Run `make run`
4. Accept any terminal prompts to delete old files

This will set up an account and run a Geth node in the console.

## Setting up miner / interacting with geth
1. Start a new console
2. Run `make cli`
3. Run `personal.unlockAccount(YOUR_ACCOUNT_HERE)`
4. Enter password `test123`
5. Run `miner.setEtherbase(YOUR_ACCOUNT_HERE)`
6. Run `miner.start()`

You should now have a working cluster and be able to interact with other accounts.

## Sending transactions
1. Run `eth.sendTransaction({from: ACCOUNT_1, to: ACCOUNT_2, value: web3.toWei(ETH_BALANCE, "ether")})`

## Deploying contracts
1. Run ``