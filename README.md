# How to integrate Marinade Liquid Staking
Documentation, repos and examples on how to integrate Marinade.Finance, from on-chain and off-chain

## Documentation

### What is Marinade?

General documentation: [docs.marinade.finance](docs.marinade.finance) 

## Integration Code Examples

### Integrating from javascript/typescript

Marinade Typescript/Javascript SDK: https://github.com/marinade-finance/marinade-ts-sdk

### Integrating from other on-chain programs

Rust, on-chain SDK: https://github.com/marinade-finance/liquid-staking-onchain-sdk

## Main Back-End code references

Technical Back-End Design Docs: https://github.com/marinade-finance/liquid-staking-program/blob/main/Docs/Backend-Design.md

### Stake

#### Deposit SOL, get mSOL
Rust Code, deposit SOL: https://github.com/marinade-finance/liquid-staking-program/blob/main/programs/marinade-finance/src/state/deposit.rs#L12

#### Depositing an existing stake account: convert a stake-account into mSOL
Rust Code, deposit stake account: https://github.com/marinade-finance/liquid-staking-program/blob/main/programs/marinade-finance/src/stake_system/deposit_stake_account.rs

### Unstake 
#### "Unstake Now!/liquid-unstake": Immediate Swap mSOL->SOL with a 0.3% fee: 
Rust Code, liquid unstaking: https://github.com/marinade-finance/liquid-staking-program/blob/main/programs/marinade-finance/src/state/liquid_unstake.rs

#### Delayed Unstake: Swap mSOL->SOL with a 0% fee, but waiting 1-2 epochs
Rust Code, delayed-unstaking: https://github.com/marinade-finance/liquid-staking-program/blob/main/programs/marinade-finance/src/state/order_unstake.rs

