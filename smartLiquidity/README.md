# Decentralized Lending Platform

This is a smart contract implementation for a decentralized lending platform using Clarity, a language for writing smart contracts on the Stacks blockchain.

## Overview

This contract allows users to deposit and withdraw sBTC (Stacks Bitcoin), borrow against their deposits, and automatically calculates interest on loans. The platform maintains a pool of deposits and manages loans for users.

## Key Features

1. Deposit sBTC
2. Withdraw sBTC
3. Borrow sBTC against deposits
4. Automatic interest calculation
5. Pool reserve for collected interest

## Contract Structure

### Maps

- `deposits`: Tracks user deposits
- `loans`: Tracks user loans and their last interaction

### Variables

- `total-deposits`: Total amount of sBTC deposited
- `pool-reserve`: Total interest collected
- `loan-interest-rate`: Current interest rate for loans (set to 10%)

### Constants

- `err-no-interest`: Error code for no interest calculation
- `err-overpay`: Error code for attempting to withdraw more than deposited
- `err-overborrow`: Error code for attempting to borrow more than deposited

### Public Functions

1. `deposit`: Allows users to deposit sBTC into the platform
2. `withdraw`: Allows users to withdraw their deposited sBTC
3. `borrow`: Allows users to borrow sBTC against their deposits

## Usage

To interact with this contract, users can call the public functions using a Stacks wallet or through a dApp interface that integrates with this smart contract.

## Notes

- The contract assumes the existence of an `asset` contract for handling sBTC transfers.
- Interest calculation logic is not fully implemented in the provided code snippet.
- Proper error handling and additional checks may be needed for production use.

## Security Considerations

- Ensure proper access controls and input validation in production.
- Thoroughly test all functions, especially those involving asset transfers.
- Consider implementing a mechanism for updating the interest rate.

## Future Improvements

- Implement full interest calculation logic
- Add liquidation mechanisms for under-collateralized loans
- Implement governance features for parameter adjustments