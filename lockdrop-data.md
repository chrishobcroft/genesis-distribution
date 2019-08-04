# Lockdrop Data

This document contains an overview of the data submitted by participants in [Edgeware's lockdrop](https://edgewa.re/lockdrop/).

The data is stored in Ethereum blockchain's chainstate.

## Signal Data

The following data is submitted as part of a **Signal** in Edgeware's Lockdrop:

| # | Name         | Type    | Data                                                                              |
|---|--------------|---------|-----------------------------------------------------------------------------------|
| 0 | contractAddr | address | Ethereum address making the signal                                                |
| 1 | nonce        | unit32  | nonce of txn when contract was created (where the signal relates to a contract)   |
| 2 | edgewareAddr | bytes   | 1 public key (hex) address without the leading 0x                                 |

## Lock Data

The following data is submitted as part of a **Lock** in Edgeware's Lockdrop.

### Lock (not Validator)

This data was submitted by a participant who **_did not elect to be a Validator_** at network launch:

| # | Name         | Type    | Data                                                                                       |
|---|--------------|---------|--------------------------------------------------------------------------------------------|
| 0 | term         | uint8   | 0 (3 months) or 1 (6 months) or 2 (12 months)                                              |
| 1 | edgewareAddr | bytes   | 1 public key (hex) address without the leading 0x                                          |
| 2 | isValidator  | bool    | false                                                                                      |

### Lock (Validator)

This data was submitted by a participant who **_elected to be a Validator_** at network launch:

| # | Name         | Type    | Data                                                                                       |
|---|--------------|---------|--------------------------------------------------------------------------------------------|
| 0 | term         | uint8   | 0 (3 months) or 1 (6 months) or 2 (12 months)                                              |
| 1 | edgewareAddr | bytes   | 3 concatenated public key (hex) addresses without the leading 0x                           |
| 2 | isValidator  | bool    | true                                                                                       |
