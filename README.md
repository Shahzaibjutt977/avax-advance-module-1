# Avalanche Local Subnet and Smart Contract Deployment

This project demonstrates how to set up a local Avalanche Subnet using `avalanche-cli` and deploy two smart contracts: `token.sol` and `vault.sol` using Remix and MetaMask.

## Prerequisites
- Golang: Install Golang for building `avalanche-cli`.
- Node.js: Install Node.js for running the local Avalanche node.
- Avalanche CLI: Follow the instructions in [Avalanche CLI Installation Guide](https://docs.avax.network/tooling/cli-guides/install-avalanche-cli) to install `avalanche-cli`.
- MetaMask: Install and configure MetaMask for connecting to the local Avalanche node.
- Remix: Open Remix and create a new workspace.

## Local Subnet Setup

### Create Subnet Configuration:

1. Run the `avalanche subnet create` command and follow the wizard to create a Subnet configuration.
2. Choose a name for your Subnet (e.g., mySubnet).
3. Select `SubnetEVM` as the VM.
4. Choose a positive integer for the ChainID (e.g., 43113).
5. Define other Subnet options as needed.

### Deploy Subnet:

1. Run the `avalanche subnet export` command to export the Subnet configuration file.
2. Run the `avalanche subnet deploy --local` command to deploy the Subnet locally.



## Smart Contract Deployment

### Compile Contracts:

1. In Remix, import the `token.sol` and `vault.sol` files.
2. Compile both contracts.

### Connect to Local Node:

1. In Remix, open the "ENVIRONMENT" dropdown in the "Deploy" tab.
2. Select "Injected Web3" and ensure MetaMask is connected to the local Avalanche node.

### Deploy Contracts:

For each contract:
1. Select the contract in the "Deployer" section.
2. Enter the constructor arguments (if any).
3. Click "Deploy".
4. Confirm the transaction in MetaMask.

### Contract Interaction:

Use the Remix interface to interact with the deployed contracts. You can call functions, read contract data, and monitor events.
