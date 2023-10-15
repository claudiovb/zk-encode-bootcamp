# Using ZoKrates to Verify Ethereum Balances in Zero-Knowledge

To generate a zkcircuit for verifying Ethereum Balances seems a non-trivial task that can be achieved with zokrates

## 1. Gather the Data
- Obtain the Merkle-Patricia Trie proof for the balance of the address in question from the Ethereum state. This proof can show the balance of the address without revealing other aspects of its transaction history.

## 2. ZoKrates DSL
- Write a ZoKrates DSL program that verifies a Merkle-Patricia Trie proof (A non funcitional initial approach is at ethVerify.zok). The program should be able to take the components of the proof as inputs (along with the Ethereum address and its claimed balance) and then verify that the proof correctly corresponds to the Ethereum state.
- Check within this program if the balance is greater than 1 ETH.

## 3. Compile and Setup
- Use ZoKrates to compile the DSL program into a set of constraints.
- Generate a proving and verification key with ZoKrates.

## 4. Generate the Proof
- Using the proving key and the Merkle-Patricia Trie proof components (as inputs to your program), generate a zkSNARK proof with ZoKrates.

## 5. Ethereum Smart Contract
- Write an Ethereum smart contract from the ZoKrates-generated verification function.

