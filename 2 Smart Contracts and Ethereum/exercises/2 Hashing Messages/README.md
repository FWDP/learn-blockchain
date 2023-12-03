## Hashing Messages

The first step in ECDSA is to hash the message before applying the signature algorithm. So if you wanted to sign a message with one your keypairs saying that you "Vote Yes on Proposal 327", the first step would be to hash this message:

```javascript
// turn this into an array of bytes, the expected format for the hash algorithm
const bytes = utf8ToBytes("Vote Yes on Proposal 327");
// hash the message using keccak256
const hash = keccak256(bytes); 

console.log(toHex(hash)); // 928c3f25193b338b89d5646bebbfa2436c5daa1d189f9c565079dcae379a43be

```

After we have the message hash we can sign it with our private key to prove that a particular address votes yes on proposal 327. You may have found yourself doing something similar if you have ever signed a message in web3. When you send a transaction to a blockchain you also sign a hashed representation of that transaction before sending it to a blockchain node.

## Your Goal: Hash the Message

The  [noble-secp256k1 library (v 1.7.1)](https://github.com/paulmillr/noble-secp256k1/tree/1.7.1)  provides us with all of the cryptography we're going to need throughout this course. Let's make use of the  `keccak256`  hash and  `utf8ToBytes`  function.

> Please note, this tutorial will require functions documented in  `release version 1.7.1`  of the  [noble-secp256k1 library](https://github.com/paulmillr/noble-secp256k1/tree/1.7.1). Any further links in this tutorial will link directly to version  `1.7.1`  of the  `noble-secp256k1`  documentation.

1.  Your first step is to take the string message passed in and turn it into an array of UTF-8 bytes. You can do so with the  `utf8ToBytes`  function.
2.  Then take the  `keccak256`  hash of those bytes and return this value.

## Adding your solution

Refer to the **template.js** file to start doing the exercise and the **Contributing** section of our main README file of this repository.

Also, the filename should be your Discord name. The file should be placed under the "1 Find Favorite Color" folder. 

Reference: [Alchemy University](https://university.alchemy.com/course/ethereum/sc/631631e2d13b2d24e60dcceb/stage/63163222d13b2d24e60dccec)