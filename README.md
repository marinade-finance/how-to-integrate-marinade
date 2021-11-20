# How to integrate Marinade Liquid Staking
Documentation, repos and examples on how to integrate Marinade.Finance, from on-chain and off-chain

## Documentation

### What is Marinade?

* General documentation: [docs.marinade.finance](docs.marinade.finance) 
* Technical Back-End Design Docs: https://github.com/marinade-finance/liquid-staking-program/blob/main/Docs/Backend-Design.md

## Integration Code Examples

### Integrating from javascript/typescript

#### Deposit SOL, get mSOL
https://github.com/marinade-finance/marinade-ts-cli/blob/main/src/marinade.ts#L110

#### "Unstake Now!/liquid-unstake": Swap mSOL->SOL with a 0.3% fee: 
https://github.com/marinade-finance/marinade-ts-cli/blob/main/src/marinade.ts#L152

### Integrating from other on-chain programs

#### Marinade on-chain SDK (NOT A PUBLIC REPO YET)
https://github.com/marinade-finance/marinade-anchor/blob/main/sdk/onchain/src/lib.rs

## Main Backend code references

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

