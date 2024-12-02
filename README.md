# darth-ton

## Notes
* If we deploy the contract with the same `code` and `data` fields as the existing smart contract, the deploying contract will merge into the existing one and have the same address as the existing one.

* Wallet - *TonKeeper*(Best)
* Environment - *Blueprint*, like *Hardhat* for *EVM Networks*
* Scanners - tonscan, tonviewer

# Contract Requests in Tonscan
AddressRequested->ResponseAddress

on testnet.tonscan
* Testnet.Non-bounceable -> X
* Testnet.Bounceable -> Testnet.Bounceable
* Mainnet.Non-bounceable -> Testnet.Bounceable
* Mainnet.Bounceable -> Testnet.Non-bounceable

on tonscan
* Testnet.Non-bounceable -> X
* Testnet.bounceable -> X
* Mainnet.Non-bounceable -> Mainnet.Non-bounceable
* Mainnet.Bounceable -> Mainnet.Non-bounceable

All these four addresses represent the same contract in both `ton.mainnet` and `ton.testnet`. Also Addresses may differ depended on wallet's version. 
Cryptographically speaking huge amount of keypairs can be generated from mother private key that is synthesized from single mnemonic. 

Accounts can have three status values
* Nonexist - When no iteraction happened with the account at all
* Uninitialized - 
