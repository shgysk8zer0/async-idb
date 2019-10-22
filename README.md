# async-idb
A promise based (async) wrapper for the IndexedDB API

[![Build Status](https://travis-ci.com/shgysk8zer0/async-idb.svg?branch=master)](https://travis-ci.com/shgysk8zer0/async-idb)
[![GitHub license](https://img.shields.io/github/license/shgysk8zer0/async-idb.svg)](https://github.com/shgysk8zer0/async-idb/blob/master/LICENSE)
![GitHub last commit](https://img.shields.io/github/last-commit/shgysk8zer0/async-idb.svg)
![GitHub release](https://img.shields.io/github/release/shgysk8zer0/async-idb.svg)

![Keybase PGP](https://img.shields.io/keybase/pgp/shgysk8zer0.svg)
![Keybase BTC](https://img.shields.io/keybase/btc/shgysk8zer0.svg)

![GitHub followers](https://img.shields.io/github/followers/shgysk8zer0.svg?style=social)
![GitHub forks](https://img.shields.io/github/forks/shgysk8zer0/async-idb.svg?style=social)
![GitHub stars](https://img.shields.io/github/stars/shgysk8zer0/async-idb.svg?style=social)
![Twitter Follow](https://img.shields.io/twitter/follow/shgysk8zer0.svg?style=social)
- - -

## Guides
- [Code of Conduct](./.github/CODE_OF_CONDUCT.md)
- [Contributing](./.github/CONTRIBUTING.md)
- [Security Policy](./.github/SECURITY.md)

## Usage
```js
import IDB from '/js/async-idb/IDB.js';

try {
  const store = await IDB.open('mydb', 1);
  const [store1, store2] = store.write('store1', 'store2', /* ... */);
  const results = await store1.add(record1, record2, /* ... */); // Uses `Promise.add` internally
  await store2.delete('somekey', 'anotherkey', /* ... */);
} catch (err) {
  console.error(err);
}

```
