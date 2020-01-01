# Supply chain & data auditing

This repository containts an Ethereum DApp that demonstrates a Supply Chain flow between a Seller and Buyer. The user story is similar to any commonly used supply chain process. A Seller can add items to the inventory system stored in the blockchain. A Buyer can purchase such items from the inventory system. Additionally a Seller can mark an item as Shipped, and similarly a Buyer can mark an item as Received.

The DApp User Interface when running should look like...

![truffle test](images/ftc_product_overview.png)

![truffle test](images/ftc_farm_details.png)

![truffle test](images/ftc_product_details.png)

![truffle test](images/ftc_transaction_history.png)


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Please make sure you've enabled MetaMask extension in your browser and gulp installed.

### Installing

A step by step series of examples that tell you have to get a development env running

Clone this repository:

```
git clone git@github.com:lnguyen-cpi/Supply-managerment.git
```

Change directory to ```project-6``` folder and install all requisite npm packages (as listed in ```package.json```):

```
cd project-6
npm install
```

Create a file name .secret and place it in current directory, and write your MetaMask seed in this file:

```
// this code will read the seed of your MetaMask seed
const mnemonic = fs.readFileSync(".secret").toString().trim();
```

Replace Infura endpoint with your own Infura account in truffle-config, remember to switch to rinkeby network first:
```
const infuraKey = "YOUR KEY HERE";
`https://rinkeby.infura.io/v3/${infuraKey}`
```

Now launch your personal supply chain to the network by following these commands:
```
$ truffle compile

$ truffle migrate --reset --network rinkeby
```

Now launch the client by the following command:
```
$ npm run dev
```

Contract address:
```
Starting migrations...
======================
> Network name:    'rinkeby'
> Network id:      4
> Block gas limit: 0x98705c


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > transaction hash:    0xa428767fd98bda57543d9a2481d0558737b9508e1be5bb2b32bbeb4df9696a8a
   > Blocks: 0            Seconds: 4
   > contract address:    0xF70D04C9Dc23F1892Af7Cbc284aDb7d89518b67a
   > block number:        5718409
   > block timestamp:     1577915502
   > account:             0xFF654511C441935A87a0A69d840c0F0e684050ef
   > balance:             21.677886837
   > gas used:            238594
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00238594 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00238594 ETH


2_deploy_contracts.js
=====================

   Deploying 'FarmerRole'
   ----------------------
   > transaction hash:    0xa32156210e94d7e8964c167ce5e9f497cd770af8d988e592d2667d7a1adbb981
   > Blocks: 0            Seconds: 9
   > contract address:    0x2465d0a3FC66061A57C32Be77077B0906BEc36fc
   > block number:        5718411
   > block timestamp:     1577915532
   > account:             0xFF654511C441935A87a0A69d840c0F0e684050ef
   > balance:             21.674102727
   > gas used:            336063
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00336063 ETH


   Deploying 'DistributorRole'
   ---------------------------
   > transaction hash:    0xba9858f6a294af7ad8438dbd4d50bf538b71c448aec7314de889ae857557c418
   > Blocks: 0            Seconds: 8
   > contract address:    0x8908fcC718b053c49e532fe9DbB2eb9c9bB525aD
   > block number:        5718412
   > block timestamp:     1577915547
   > account:             0xFF654511C441935A87a0A69d840c0F0e684050ef
   > balance:             21.670741857
   > gas used:            336087
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00336087 ETH


   Deploying 'RetailerRole'
   ------------------------
   > transaction hash:    0x7c94d54d4642e066eab1d3e105ab5579d11d52cfc0d9253635eed6eb775739d1
   > Blocks: 0            Seconds: 8
   > contract address:    0xF3de70448058dC148b9E5aFd7cf9E98669cc5ef2
   > block number:        5718413
   > block timestamp:     1577915562
   > account:             0xFF654511C441935A87a0A69d840c0F0e684050ef
   > balance:             21.667380747
   > gas used:            336111
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00336111 ETH


   Deploying 'ConsumerRole'
   ------------------------
   > transaction hash:    0x95d4fdd48f59f1118b3e08e61fa6246ba7852564e653ca9e8804eaadc8a9fd72
   > Blocks: 0            Seconds: 12
   > contract address:    0x64bd2811526D9Aeb6847794B2A3D0a4a3230f492
   > block number:        5718414
   > block timestamp:     1577915577
   > account:             0xFF654511C441935A87a0A69d840c0F0e684050ef
   > balance:             21.664019877
   > gas used:            336087
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00336087 ETH


   Deploying 'SupplyChain'
   -----------------------
   > transaction hash:    0x183c7dab6b9e65d31046e3c60259cbc0fcabb055f691f06646682a8ff03987f5
   > Blocks: 0            Seconds: 8
   > contract address:    0xf61df456C7ac5E4ADcf1Dea00Ee7031866Db7094
   > block number:        5718415
   > block timestamp:     1577915592
   > account:             0xFF654511C441935A87a0A69d840c0F0e684050ef
   > balance:             21.636380107
   > gas used:            2763977
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.02763977 ETH


   Deploying 'Ownable'
   -------------------
   > transaction hash:    0x7141a6e495236f4e6ef9e369b08a3d73387d57738a21c0269cd77c5bb69f3658
   > Blocks: 0            Seconds: 8
   > contract address:    0xE534EBD7472c6A509D92460c86bDEc9E462B2EF1
   > block number:        5718416
   > block timestamp:     1577915607
   > account:             0xFF654511C441935A87a0A69d840c0F0e684050ef
   > balance:             21.633451257
   > gas used:            292885
   > gas price:           10 gwei
   > value sent:          0 ETH
   > total cost:          0.00292885 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:           0.0440121 ETH


Summary
=======
> Total deployments:   7
> Final cost:          0.04639804 ETH
```

## Built With

* [Ethereum](https://www.ethereum.org/) - Ethereum is a decentralized platform that runs smart contracts
* [IPFS](https://ipfs.io/) - IPFS is the Distributed Web | A peer-to-peer hypermedia protocol
to make the web faster, safer, and more open.
* [Truffle Framework](http://truffleframework.com/) - Truffle is the most popular development framework for Ethereum with a mission to make your life a whole lot easier.


## Authors

See also the list of [contributors](https://github.com/your/project/contributors.md) who participated in this project.

## Acknowledgments

* Solidity
* Ganache-cli
* Truffle
* IPFS
