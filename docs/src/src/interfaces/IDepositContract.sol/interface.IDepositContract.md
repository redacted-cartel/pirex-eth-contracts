# IDepositContract
## General Overview
- This interface is designed to interact with the Ethereum 2.0 deposit contract, which is used for staking and participating in the Ethereum 2.0 (Eth2) Beacon Chain.
- For more information see the Phase 0 specification under https://github.com/ethereum/eth2.0-specs

## Technical Overview


## Functions
### deposit

Submit a Phase 0 DepositData object.


```solidity
function deposit(
    bytes calldata pubkey,
    bytes calldata withdrawal_credentials,
    bytes calldata signature,
    bytes32 deposit_data_root
) external payable;
```
**Parameters**

|Name|Type|Description|
|----|----|-----------|
|`pubkey`|`bytes`|A BLS12-381 public key.|
|`withdrawal_credentials`|`bytes`|Commitment to a public key for withdrawals.|
|`signature`|`bytes`|A BLS12-381 signature.|
|`deposit_data_root`|`bytes32`|The SHA-256 hash of the SSZ-encoded DepositData object. Used as a protection against malformed input.|


### get_deposit_count

Query the current deposit count.


```solidity
function get_deposit_count() external view returns (bytes memory);
```
**Returns**

|Name|Type|Description|
|----|----|-----------|
|`<none>`|`bytes`|The deposit count encoded as a little endian 64-bit number.|


