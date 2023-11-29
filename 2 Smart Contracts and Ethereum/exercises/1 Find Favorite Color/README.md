# Find Favorite Color

Cryptographic Hash Functions like SHA256 are one-way functions. This means that if you have the input, it's relatively trivial to find the output. On the other hand, if you have the output, it is infeasible to find the input.
 

However, if you knew the hashes of some common inputs, then you could brute-force guess at the output or create a Rainbow Table to determine what that input is.
 

It's easy to find that the SHA256 hash of "apples" is ``0xf5903f...0f74d9.`` If this was a likely input, a hacker could search for it specifically and know that the input was "apples"!

> For security purposes, it's important to remember to use a random **salt** which you can add to your input to make it unguessable via the methods mentioned above!

## ## Your Goal: Find the Color

Given a SHA256 hash, find the color input that would generate that hash. You can assume that all the hashes be generated only from colors provided in the  `COLORS`  array.

1.  To take the hash of a color, first use  `utf8ToBytes`  to translate the string to bytes. Then, use  `sha256`  to hash it.
2.  When you want to compare two hashes, first use  `toHex`  to turn each hash from a  [Uint8Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Uint8Array)  to a string of hexadecimal characters.

So comparing two hashes would look like this:

```javascript
const a = "apple";
const b = "banana";

const aBytes = utf8ToBytes(a);
const bBytes = utf8ToBytes(b);

const aHash = sha256(aBytes);
const bHash = sha256(bBytes);

console.log(toHex(aHash) === toHex(aHash)); // true
console.log(toHex(aHash) === toHex(bHash)); // false
```

>Wondering what utf8 stands for? The UTF-8 standard translates all the possible keyboard characters you can think of into bytes. This is an agreed upon standard to ensure we all get the same bit values representing the letters and words we see on the screen. Learn more about [utf8 here](https://en.wikipedia.org/wiki/UTF-8).

Refer to the **template.js** file to start doing the exercise.

Reference: [Alchemy University](https://university.alchemy.com/course/ethereum/sc/6317afca5216a46480f65674/stage/6317afca5216a46480f65677)