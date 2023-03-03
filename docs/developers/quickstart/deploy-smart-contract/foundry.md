---
title: Foundry
sidebar_position: 3
---

# Foundry

In this tutorial, we'll walk through creating a basic [Foundry](https://book.getfoundry.sh/) project.

## Prerequisites

Before you begin, Ensure you've:

1. [Set up your wallet](../../../use-zkevm/set-up-your-wallet.md)
1. [Funded your wallet with goerli ETH](../../../use-zkevm/fund.md)
1. [Bridged Goerli ETH to ConsenSys zkEVM](../../../use-zkevm/bridge-funds.md)
1. Downloaded Foundry using the following command:

   ```bash
   curl -L https://foundry.paradigm.xyz | bash
   ```

   Then, open a new terminal, and call `foundryup` to install the latest release.

## Create a Foundry project

To create an empty Foundry project, run:

```bash
forge init zkevm-tutorial
```

## Write the smart contract

`forge init` sets you up with a sample contract, test, and script for `Counter.sol`. To build it, simply run `forge build`.

## Deploy the smart contract

To deploy a smart contract, run:

```bash
forge create --rpc-url https://consensys-zkevm-goerli-prealpha.infura.io/v3/INFURA_API_KEY --private-key YOUR_PRIVATE_KEY src/Counter.sol:Counter
```

:::info

Ensure you replace `INFURA_API_KEY` and `YOUR_PRIVATE_KEY` in the above command.

:::

Your output should look a little something like this:

```bash
Deployer: YOUR_ACCOUNT_NUMBER
Deployed to: 0xED0Ff7E8B655dFFfCA471ea3B6B649ce7C2C1b83
Transaction hash: 0x967e1290b285e67b3d74940ee19925416734c345f58bd1ec64dcea134647d7ee
```