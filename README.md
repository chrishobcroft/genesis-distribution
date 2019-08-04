![hero-black](https://user-images.githubusercontent.com/2212651/62415240-cb758580-b626-11e9-8c3b-1a715c7b5cfc.png)

# Straightedge Genesis Distribution

This repository contains contributions from the Straightedge Launch Community, to the process of agreeing and generating the genesis distribution, and hence the genesis block to be validated at the launch of the Straightedge chain.

## Overview

When the Straightedge chain launches, Validators in the network will launch the Straightedge software, which will validate a **genesis block file**.

This **genesis block file** will contain the initial **"genesis" distribution** of STR tokens (amongst other things).

This **genesis block file** will be created using:

1. addresses and data from Edgeware's lockdrop, stored in Ethereum blockchain

  - This can be defined algorithmically, based on a set of parameters and code to parse Ethereum blockchain's chainstate
  
  - See [lockdrop data](./lockdrop-data.md) for an overview of this data

2. allocations to addresses owned by participants in the Straightedge Launch Community

  - The amounts allocated to these addresses has not yet been finalised

  - Technically, this will only be finalised when the chain launches...!

## Purpose of this repo

This repository is to receive contributions from the Straightedge Launch Community, to design and create a process to

- parse Edgeware's lockdrop data from Ethereum blockchain

- calculate allocations of STR to addresses of lockdrop participants (signals, locks)

- include allocation to addresses of Straightedge Launch Community participants

## Community Survey

This project is collecting opinions regarding the genesis distribution for Straightedge.

If you would like to participate, please follow [this link](https://communitygovernance.typeform.com/to/oKZtnC).
