# 00-Warmup

A Bitcoin block contains mainly two parts: a header, and a list of transactions.

The header contains the following information about a block:
- the version of the Bitcoin protocol,
- the previous block's header hash,
- the Merkle root of the transactions,
- the time when the block was created,
- the difficulty value used for mining the block,
- a nonce, which is an arbitrary number.

The Merkle root is a hash obtained from the transactions in the block. Conceptually a Merkle tree is a binary tree, with bottom layer nodes representing hashes of transactions, and every other node representing a hash that combines the hashes of its children. The Merkle root is the hash value at the root.

For a Merkle tree with 3 transactions, here's a graphical representation of the tree:

```
          a
         / \
        /   \
       /     \
      /       \
     b         c
    / \       /
   /   \     /
  d     e   f
  |     |   |
  1     2   3
```
Here, 1, 2, and 3 are transactions, d, e, f represent hashes of the transactions, and a, b and c represent hashes that come from their respective child/children.

For this exercise, the Merkle tree is represented by a literal binary tree. You may check out `bitcoin_utils.h` to find definitions of relevant structs.

The process of "mining" Bitcoin involves a brute force process, and the goal is to find a hash for the header that is smaller than the target value (usually explained to people as "having a certain number of leading zeros"). The "nonce" value is incremented on each loop, which changes the hash of the block header.

## Task description

First, compile and run the code template as is. The template will create a Bitcoin block with the same data as the real Bitcoin's genesis block, and print the header in a human-readable format.

The printed data should look something like this:

```
====Debug print header start====
version:       1
prev blk hash: 0000000000000000000000000000000000000000000000000000000000000000
merkle root:   3BA3EDFD7A7B12B27AC72C3E67768F617FC81BC3888A51323A9FB8AA4B1E5E4A
timestamp:     1231006505 (2009-01-04 02:15:05 (CST))
difficulty:    1D00FFFF
nonce:         2083236893
====Debug print header end====
```

After that, modify the code to complete the following tasks:
- Construct a Merkle tree, using the transaction data provided in the template. The data nodes and one hash node has been created for you, and you need to create the rest of the hash nodes and set their relevant pointers.
- Uncomment the block comment near the bottom of the code, and set `my_blcok->merkle_tree` to the root node of your Merkle tree.
- Write a brute force loop to find a valid nonce for the block.

It should take a few seconds for your computer to find a valid nonce. If it feels too fast or too slow, you may change the difficulty value near the top of the `main` function, in the `difficulty` variable. The `DIFFICULTY_1M` macro makes it take on average 1 million attempts to find a valid nonce; and a few other macros are defined in `bitcoin_utils.h`.