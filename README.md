# go-frkhash

Frkhash go module intended for use by core-pool (and open-ethereum-pool).

* for core-pool see https://github.com/etclabscore/open-etc-pool
* for more information on frkhash see https://github.com/eth-classic/frkhash
* supports frkhash, ethash & ubqhash

### usage (frkhash)

```go
var ecip1099FBlockClassic uint64 = 11700000 // classic mainnet
var ecip1099FBlockMordor uint64 = 2520000 // mordor testnet

var hasher = frkhash.New(&ecip1099FBlockMordor, nil)

if hasher.Verify(block) {
    ...
}
```

### usage (ethash)

```go
var hasher = frkhash.New(nil, nil)

if hasher.Verify(block) {
    ...
}
```

### usage (ubqhash)

```go
var uip1FEpoch uint64 = 22 // ubiq mainnet

var hasher = frkhash.New(nil, &uip1FEpoch)

if hasher.Verify(block) {
    ...
}
```

