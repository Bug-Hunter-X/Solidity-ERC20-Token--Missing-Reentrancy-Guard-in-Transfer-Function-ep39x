# Solidity ERC20 Token: Reentrancy Vulnerability

This repository demonstrates a common vulnerability in Solidity smart contracts: the lack of a reentrancy guard in the `transfer` function of an ERC20 token.  A reentrancy attack allows an attacker to repeatedly call the `transfer` function before the state changes from the previous call are finalized, leading to theft of tokens.

The `bug.sol` file shows the vulnerable implementation. The `bugSolution.sol` demonstrates how to fix this vulnerability using the Checks-Effects-Interactions pattern.