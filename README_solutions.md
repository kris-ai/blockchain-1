node 1
pass: impakkt33
public address: 0xa9CcfAa94C61ed2ffFe17b529fDB25e229A364F7
Path of the secret key file: node1/keystore/UTC--2021-02-02T05-09-39.612731000Z--a9ccfaa94c61ed2fffe17b529fdb25e229a364f7

enode://07d222c7f70139e47bf9a8010e1967e06075f440f95a5e56088c90211ed6c43bfd26aa013410219753a9f71d84a154e43ed4054ae1c399cd03de13873c8d1083@127.0.0.1:30303

node 2
pass: impakkt34!
public address: 0xF8C44C168A7E1C8a73b88c12d7b466ff7f256132
Path of the secret key file: node2/keystore/UTC--2021-02-02T05-12-23.313288000Z--f8c44c168a7e1c8a73b88c12d7b466ff7f256132


network name: impakkt
chain id = 39508



explains how to start the network.

blockchain-tools/geth --datadir node1 init ./impakkt/impakkt.json

blockchain-tools/geth --datadir node2 init ./impakkt/impakkt.json

blockchain-tools/geth --datadir node1 --unlock "0xa9CcfAa94C61ed2ffFe17b529fDB25e229A364F7" --mine --rpc --allow-insecure-unlock

blockchain-tools/geth --datadir node2 --unlock "0xF8C44C168A7E1C8a73b88c12d7b466ff7f256132" --mine --port 30304 --bootnodes "enode://07d222c7f70139e47bf9a8010e1967e06075f440f95a5e56088c90211ed6c43bfd26aa013410219753a9f71d84a154e43ed4054ae1c399cd03de13873c8d1083@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock


Remember to include any environment setup instructions and dependencies.

Be sure to include all of the geth flags required to get both nodes to mine and explain what they mean.

Explain the configuration of the network, such as it's blocktime, chain ID, account passwords, ports, etc.

Explain how to connect MyCrypto to your network and demonstrate (via screenshots and steps) and send a transaction.
