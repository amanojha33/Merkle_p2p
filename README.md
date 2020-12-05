# Merkle_p2p
A distributed p2p networking subsystem with Merkle tree as hash-based data structure and SHA-256 encryption methodology.  

Merkle Trees are also really efficient. They allow us to compress large data sets by removing all superfluous branches while keeping only the ones we need to establish our proof.

![alt text](/docs/merkle.png)

A Merkle Tree is a complete binary tree which is used by Cryptocurrency SPV Wallets. SPV allows a lightweight client to verify that a transaction is included in the Bitcoin blockchain, without downloading the entire blockchain.

By using a merkle tree, one can validate a large data set contained inside the tree by just comparing the merkle root / root node of the tree.

This script assumes the input data is in the form of CSV File, and saves the finally calculated merkle root for the user in another CSV File.

The data is stored in the leaf nodes and we bubble up from botton to top by calculating the hash of each leaf node.

At the end we are left with a single merkle root capable of validating the whole data set with just a single hash string of 32 bytes.

# Performance of the Script

For a CSV File with 1000 rows it takes 1.1 sec to get merkle root.
(The script doesn't support validation currently, just merkle root calculation using sha256 hashing)