# Project #5. Decentralized Star Notary

This is Project provides a Star Notary DAPP deployed on Rinkeby testnet.

## Dependencies
The main project dependencies are:
 * Truffle. See https://www.npmjs.com/package/truffle
 * OpenZeppelin. See https://www.npmjs.com/package/openzeppelin-solidity
 * Webpack dev server library. See https://www.npmjs.com/package/webpack-dev-server
 
 ### Versions
 * truffle version: v5.0.12
 * openzeppelin-solidity version: v2.2.0
 
## Deployment
* Create `.secret` file in root directory and paste secret phrase
### `truffle-config.js` config
* Update infuraKey variable
* Set network configuration in network map
```json5
e.g
...
  network: {
  ...
    rinkeby: {
       provider: () => new HDWallet(mnemonic, `https://rinkeby.infura.io/v3/${infuraKey}`),
       network_id: 4, // rinkeby's id
       gas: 4500000,  // rinkeby has a lower block limit than mainnet
       gasPrice: 10000000000
       timeoutBlocks: 300,  // # of blocks before a deployment times out  (minimum/default: 50)
       skipDryRun: true
    }
    ...
  }
```

* Run `truffle migrate --reset --network <NETWORK_NAME>`
## How to install App
* Run `cd app && npm install dev` 

## Running the app
* Run `npm run dev` from `app` directory

### Token Information
* Token Name: Star Gazer
* Token Symbol: STG
* Token Address on Rinkeby Network: 0x071633471c2846371E33557D68B1F28C63aE976C
