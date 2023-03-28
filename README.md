# Cli

A command tool for operator.

## Install 

### golbal 

```
$ yarn global add @polkadot/api-cli
$ polkadot-js-api ...
```

### base npx
```
npm install
```

## Examples

### Account seed

```
  Secret seed:      0x464483dd65fb6e6f171cb0ee059cc8e12c3966ffcbc340960ab13e89001e332d
  Public key (hex): 0x03cbf84b7b9b052aa27ddc4ba6c15e1c04cb56c1d1d97764489c2718041602ee9a
  Account ID:       0x2f7f4875b4a89aa445e0ebf03edcd8628c984f78
```

* transfer tBOL

```shell
docker run -it --rm bnk-cli polkadot-js-api --types types.json --ws ws://<HOST_IP>:9944 --seed 0x5fb92d6e98884f76de468fa3f6278f8807c48bebc13595d45af5bdc4da702133  --sign ethereum tx.balances.transfer 0x2f7f4875b4a89aa445e0ebf03edcd8628c984f78  0xffffffffffffffff
```

* bond account
  
```shell
npx polkadot-js-api --types types.json --ws ws://127.0.0.1:9944 --seed 0x464483dd65fb6e6f171cb0ee059cc8e12c3966ffcbc340960ab13e89001e332d  --sign ethereum tx.staking.bond 0x2f7f4875b4a89aa445e0ebf03edcd8628c984f78  0xfffffffffffffffff Staked
```

* become a validator

```shell
npx polkadot-js-api --types types.json --ws ws://127.0.0.1:9944 --seed 0x464483dd65fb6e6f171cb0ee059cc8e12c3966ffcbc340960ab13e89001e332d  --sign ethereum tx.staking.validate '{"commission":1000000000,"blocked":false}'
```

* exit validator

```shell
npx polkadot-js-api --types types.json --ws ws://127.0.0.1:9944 --seed 0x464483dd65fb6e6f171cb0ee059cc8e12c3966ffcbc340960ab13e89001e332d  --sign ethereum tx.staking.chill
```