# IBC Hack 1 - ink! Smart Contracts in Rust

## Download and run the contracts-node:

Follow the intructions below to run the subtrace-contracts-node either on Linux or on Mac OS:

### On Linux:

1. Download contracts node: 

    ```
    curl -O -L https://github.com/paritytech/substrate-contracts-node/releases/download/v0.19.0/substrate-contracts-node-linux.tar.gz
    ```

2. Unpack:

   ```
   tar -xzf substrate-contracts-node-linux.tar.gz
   ```

3. cd into dir:

   ```
   cd artifacts/substrate-contracts-node-linux
   ```

4. Run node: 
   ```
   ./substrate-contracts-node --dev
   ```
   

### On Mac OS:

1. Download contracts node: 

    ```
    curl -O -L https://github.com/paritytech/substrate-contracts-node/releases/download/v0.19.0/substrate-contracts-node-mac-universal.tar.gz
    ```

2. Unpack:

   ```
   tar -xzf substrate-contracts-node-mac-universal.tar.gz
   ```

3. cd into dir:

   ```
   cd artifacts/substrate-contracts-node-mac
   ```

4. Run node: 
   ```
   ./substrate-contracts-node --dev
   ```
   
## Open flipper Smart Contract in ink! Playground:

Open the standard flipper Smart contract in ink! Playground here (open in new tab): [here](https://ink-playground.substrate.io)

## Exercise 1: compile and deploy a Smart Contract

The ink! playground browser IDE loads with the flipper contract. This is ink!'s very basic example of a Smart Contract. It holds one `bool` variable which can be either read through `get()` or flipped from `true` to `false` and vice versa through `flip()`.

1. Click on Test button, the tests should pass
2. Click on Compile button, the Smart Contract should compile
3. Download the .contract bundle
4. Click on the Deploy on Contracts UI button
5. Deploy the Smart Contract
6. Interact with the Smart Contract: read the state variable, flip it, read it again

## Exercise 2: modify the Smart Contract

We want to modify the basic flipper example such that we replace the `bool` state variable by a `i8` and change the `flip()` extrinsic to a `set()` extrinsic which allows us to set a specific value.

1. Change the state variable from `bool` to `i8`
2. Rename `flip(&mut self)` to `set(&mut self, value: i8)`
3. Make the Smart Contract compile
4. Fix the tests

