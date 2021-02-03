# Rollups and Their Guarantees

Curated list of rollups on Ethereum and their security guarantees. This list is specifically about two guarantees: _permissionlessness_ and _upgradability_. In other words, **it is not an exhaustive list of properties** and should not be considered as such. All projects come with tradeoffs.

## How to Read

- **Project**: project name.
- **Permissionless?**: whether using the rollup is permissionless. Permissionless withdrawals don't count, neither do permissionless single transactions (since you're not getting the benefit of the rollup in that case).
- **Upgradable?**: whether the contracts are upgrdable via admin keys or governance in a way that can compromise user funds. Having timeouts still counts.

- ✔️ Green checkmark means "good," with details following.
- ❌ Red cross means "bad," with details following.
- ❓ Question mark means "insufficient data for meaningful answer."

## List

| Project | Permissionless? | Upgradable? |
|---|---|---|
| [Arbitrum](https://github.com/OffchainLabs/arbitrum) | ✔️ [Yes](https://github.com/OffchainLabs/arbitrum/blob/de2878de27c6fbb8705110649c7708ce926c98e8/packages/arb-bridge-eth/contracts/rollup/Staking.sol#L276-L285) | ✔️ [No](https://github.com/OffchainLabs/arbitrum/blob/de2878de27c6fbb8705110649c7708ce926c98e8/packages/arb-bridge-eth/contracts/rollup/ArbRollup.sol) |
| [Fuel](https://github.com/FuelLabs/fuel) | ✔️ [Yes](https://github.com/FuelLabs/fuel/blob/49c35e8de752200175174a08b6a8eae42796790d/src/Block.yulp#L95-L101) | ✔️ [No](https://github.com/FuelLabs/fuel/blob/49c35e8de752200175174a08b6a8eae42796790d/src/Fuel.yulp) |
| [Hermez](https://github.com/hermeznetwork/contracts) | ✔️ [Yes](https://github.com/hermeznetwork/contracts/blob/89fa4073f3a714a318fb035a5f62446573f9d210/contracts/hermez/Hermez.sol#L279-L283) | ❌ [Yes](https://github.com/hermeznetwork/contracts/blob/master/contracts/upgradability/Timelock.sol) |
| [Loopring](https://github.com/Loopring/protocols/tree/master/packages/loopring_v3) | ❌ [No](https://github.com/Loopring/protocols/blob/bbcebc4848b4a1c5ba8264a2d601de5f8183b5aa/packages/loopring_v3/contracts/core/impl/ExchangeV3.sol#L340) | ❌ [Yes](https://github.com/Loopring/protocols/blob/ca90ef68a9d5e70f75d6afe70f29d64be179450b/packages/loopring_v3/contracts/core/impl/LoopringV3.sol#L171) |
| [Optimism](https://github.com/ethereum-optimism/optimism-monorepo) | ❌ [No](https://github.com/ethereum-optimism/contracts-v2/blob/e8bf5902c7d3a1dfed165e2196ef98acca8ff6a3/contracts/optimistic-ethereum/OVM/chain/OVM_CanonicalTransactionChain.sol#L298-L299) | ❌ [Yes](https://medium.com/ethereum-optimism/mainnet-soft-launch-7cacc0143cd5) |
| [Starkware](https://github.com/starkware-libs/starkex-contracts) | ❓ | ❓ [Maybe](https://github.com/starkware-libs/starkex-contracts/tree/210284a0b95fab6abcf25bc1a2f1b7b98cea0b78/scalable-dex/contracts/src/upgrade) |
| [zkSync](https://github.com/matter-labs/zksync) | ❌ [No](https://github.com/matter-labs/zksync/blob/1cda8c7c1a9bfbec6491a1e4634b0fc33b206834/contracts/contracts/ZkSync.sol#L268) | ❌ [Yes](https://github.com/matter-labs/zksync/blob/1cda8c7c1a9bfbec6491a1e4634b0fc33b206834/contracts/contracts/ZkSync.sol#L78-L80) |
