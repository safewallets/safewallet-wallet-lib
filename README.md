# safewallet-wallet-lib

[![Build status](https://img.shields.io/travis/particle4dev/safewallet-wallet-lib/master.svg?style=flat-square)](https://travis-ci.org/particle4dev/safewallet-wallet-lib)

### How to build Safewallet lib for client side

install browserify

```console
browserify index.js --standalone safewallet > safewalletlib.js
```

### How to add btc compatible pow coin
- add coin network params to src/bitcoinjs-networks.js
- add electrum servers list to src/electrum-servers.js
- add tx fee to src/fees.js
- add an explorer link to src/coin-helpers.js

### How to add safe asset chain
- add electrum servers list to src/electrum-servers.js
- add tx fee to src/fees.js
- add asset chain ticker and an explorer link to src/coin-helpers.js

### How to add ERC20 token
- add token contract id to src/eth-erc20-contract-id.js
- add token decimals value to src/eth-erc20-decimals.js, read instructions

### How build for old browsers (ES5)
install babel cli

```console
npm run build
```

example:
`var fromSats = require('safewallet-wallet-lib/build/utils').fromSats;`
