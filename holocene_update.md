# Holocene Network Upgrade
---

## Stop Old Containers
```
cd unichain-node
```
```
docker compose down -v
```

## Update to latest release
```
git stash
```
```
git pull
```

## Edit files
```
nano .env.sepolia
```
- Change the rpc url
- OP_NODE_L1_ETH_RPC=https://ethereum-sepolia-rpc.publicnode.com
- OP_NODE_L1_BEACON=https://ethereum-sepolia-beacon-api.publicnode.com
- Ctrl X Y Enter

```
nano .env
```
- Delete all of the codes and paste this 
```
HOST_DATA_DIR=/$HOME/root/unichain-node/geth-data
HOST_NODE_DATA_DIR=/$HOME/root/unichain-node/opnode-data
```
- Ctrl X Y Enter

## Run the Node
```
docker compose up -d
```

## Save Node PrivateKey:
```
cat $HOME/unichain-node/geth-data/geth/nodekey
```

- Note: For any daemon related port error you can follow our old video for solution: [Youtube](https://youtu.be/L2NL1U6DujI?si=pW2VS4Y8I5cM3zhI)

---
- Done !! Feel free to ask queries in telegram channel
- Telegram - https://t.me/colony_airdrops
- Youtube - https://www.youtube.com/@ColonyAirdrops
