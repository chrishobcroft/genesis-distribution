![hero-black](https://user-images.githubusercontent.com/2212651/62415240-cb758580-b626-11e9-8c3b-1a715c7b5cfc.png)

# Straightedge Genesis Block Generation Script

This repository contains contributions from the Straightedge Launch Community, to the process of generating the genesis block file to be used to launch the Straightedge chain.

## Overview

The **initial distribution** of STR tokens will be contained in the **genesis block file**, which will be used by Validators to launch the Straightedge chain.

This **genesis block file** will be created using:

1. data from Edgeware's lockdrop, stored in Ethereum blockchain
2. agreed allocation to Straightedge Launch Community

This repository is to receive contributions from the Straightedge Launch Community, to design and create a process to

- parse Edgeware's lockdrop data from Ethereum blockchain

- calculate allocations of STR to addresses of lockdrop participants (signals, locks)

- include allocation to addresses of Straightedge Launch Community participants

## Lockdrop Data

The following data is submitted as part of a **Signal** in Edgeware's Lockdrop:

| # | Name         | Type    | Data                                                                              |
|---|--------------|---------|-----------------------------------------------------------------------------------|
| 0 | contractAddr | address | Ethereum address making the signal                                                |
| 1 | nonce        | unit32  | nonce of txn when contract was created (where the signal relates to a contract)   |
| 2 | edgewareAddr | bytes   | 1 address e.g. 0x0a5a3bf8f1f79397839091b54badc08b395b50607df6b9f6312af6b7ddc1fb3d |

The following data is submitted as part of a **Lock** in Edgeware's Lockdrop, for a participant who **_did not elect to be a Validator_** at network launch:

| # | Name         | Type    | Data                                                                                       |
|---|--------------|---------|--------------------------------------------------------------------------------------------|
| 0 | term         | uint8   | 0 (3 months) or 1 (6 months) or 2 (12 months)                                              |
| 1 | edgewareAddr | bytes   | 1 Public key (hex) address without the leading 0x                                          |
| 2 | isValidator  | bool    | false                                                                                      |

The following data is submitted as part of a **Lock** in Edgeware's Lockdrop, for a participant who **_elected to be a Validator_** at network launch:

| # | Name         | Type    | Data                                                                                       |
|---|--------------|---------|--------------------------------------------------------------------------------------------|
| 0 | term         | uint8   | 0 (3 months) or 1 (6 months) or 2 (12 months)                                              |
| 1 | edgewareAddr | bytes   | 3 concatenated Public key (hex) addresses without the leading 0x                           |
| 2 | isValidator  | bool    | true                                                                                      |false
