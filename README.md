# Merkle_p2p
A distributed p2p networking subsystem with Merkle tree as hash-based data structure and SHA-256 encryption methodology. 

Merkle Trees are also really efficient. They allow us to compress large data sets by removing all superfluous branches while keeping only the ones we need to establish our proof. In the Blockchain world, this means Merkle Trees provide the following critical features:
-Ability to verify whether a transaction is included in a block
-Light-clients (since we don’t have to download the entire chain)
-Overall performance and scalability
-Simplified Payment Verification or (SPV)

