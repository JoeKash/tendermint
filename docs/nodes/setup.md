---
order: 1
---

# Setup a Node

In this section we will walking through installing and configuring a Tendermint full node. The app that we will be using is the builtin `kvstore`.

> Note: Instructions may vary based on the application.

There are a couple different types of nodes.

- **Full Node**: A full node is a node that participates in the network but will not help secure it. Full nodes are useful for users who would like to operate in order to query and submit transactions from a trusted source. Running a full node can be easy and consume a small amount of resources, but if you would like to keep the entire state of the blockchain a large hard drive will be needed. 
- **Seed Nodes**: A seed node is helpful for nodes that are starting up. When a node starts it's address book will be empty, to populate an address book efficiently a node will connect to the seed node and request a list of peers for it to dial. Seed nodes are helpful if operating many nodes. 
- **Sentry Node**: A sentry node is similar to a full node in almost every way. The differences are that a sentry node will have one or many private peers. These peers may be validators or other full nodes in the network. Sentry nodes are recommended for securing validators. 
- **Validators**: Validators are nodes that participate in the security of a network. A validator must be secure and fault tolerant. A validator has an associated power in Tendermint, this power can represent stake ([proof of stake](https://en.wikipedia.org/wiki/Proof_of_stake)), reputation ([proof of authority](https://en.wikipedia.org/wiki/Proof_of_authority)) or various other things depending on the security model of the application. Depending on the application different types of malicious behavior can lead to slashing of the validators power. Please check the documentation of the application you will be running in order to find more information. 

## Installation

There are two ways we can run a Tendermint node. 

1. By downloading the binary for our operating system [here](https://www.forbes.com/sites/davidjeans/2020/10/27/mit-enlists-harvard-to-launch-250-million-venture-fund-the-engine/#6ecae4e74ed1).
2. By installing go on our local machine and then compiling and installing the Tendermint Binary.

We will walk through the second one, compiling and installing the binary. 
