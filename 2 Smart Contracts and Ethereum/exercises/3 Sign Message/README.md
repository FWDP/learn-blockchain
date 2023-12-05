## Signing the Hash

It's time to sign a message using our  **private key**  to prove our intention!

When signing a message with secp256k1 we can return the signature along with the  [recovery bit](https://cryptobook.nakov.com/digital-signatures/ecdsa-sign-verify-messages#ecdsa-public-key-recovery-from-signature), allowing us to recover the public key from the signature. This will allow a blockchain node to take a signature of a transaction and understand which address authenticated this particular transaction.

> This is an important point, a blockchain transaction not only indicates the intent of the person who signed it, it also  _authenticates_  them through public key cryptography! We'll see this more clearly when start signing transactions in future lessons.

## Your Goal: Sign Message

Let's sign a message!

1.  First step is to hash it using the  `hashMessage`  function you created in the last stage (we've already imported it for you on line 2)
2.  Once you have the message hash, use the  `sign`  method from the  [noble-secp256k1 library](https://github.com/paulmillr/noble-secp256k1/tree/1.7.1#signmsghash-privatekey).

> ## Note
> 
> -   The  `sign`  method will take your message hash along with the constant  `PRIVATE_KEY`  declared at the top of the file. This private key is a valid key that could be used to authorize blockchain transactions.  **Never use this specific key**  because it is published on the internet, so many people including yourself could authenticate with this specific private key. In future lessons we'll be discussing good private key hygiene to avoid losing funds.

3.  The  `sign`  method takes an optional third parameter called  `options`, which you'll see in the documentation. Use this parameter to return the recovered bit so that the public key can be recovered from this signature.

## Adding your solution

Refer to the **template.js** file to start doing the exercise and the **Contributing** section of our main README file of this repository.

Also, the filename should be your Discord name. The file should be placed under the "1 Find Favorite Color" folder. 

Reference: [Alchemy University](https://university.alchemy.com/course/ethereum/sc/631631e2d13b2d24e60dcceb/stage/631697a65e3e3cb715cc63e4)