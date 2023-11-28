# Introduction to Blockchain

## What is blockchain?
 
The blockchain is a special kind of database that stores transactions chronologically. Think of what happens in a bank, where a transaction is usually composed of a sender, receiver, and bank. The bank authorizes the transaction as it acts as a central authority.

<img src="../assets/Centralized transaction.PNG" alt="Image of centralized transaction" />

In the case of blockchain, transactions are chained or linked with the previous ones. Each transaction is stored in a "block." So, intuitively, blockchain is the "chain of blocks." It is protected by cryptography, the process of hiding information from outsiders. There is no central authority; it's a decentralized, immutable ledger (an immutable ledger means that the records cannot be changed).

<img src="../assets/Blockchain.PNG" alt="Image of centralized transaction" />

What verifies the transaction is the public network of computers. It is labeled as the consensus mechanism, where all nodes will reach an agreement.

## Blockchain Network


The term "decentralized" implies that participants in the network collaborate to ensure the legitimacy of newly introduced blocks and prevent fraud. Specifically, 51% of all participants, each possessing a copy of the new block for cross-referencing, must validate its legitimacy within the network. Once verified, all clients obtain a copy of the new block, and it becomes accepted within the network. This approach reduces the necessity for transaction fees, ensuring network security. However, it's worth noting that transaction fees are occasionally utilized as incentives for miners (participants) to validate transactions and sustain the network.

> References 
> [Learn the Basics of Blockchain with Python | Codecademy](https://www.codecademy.com/courses/introduction-to-blockchain/lessons/blockchain-introduction/exercises/what-is-blockchain)