# Blockchain definition
Blockchain is a list of records, called *blocks*, that are securely linked together using cryptography. Each blocks contains a cryptographic hash of the previous block, a *timestamp*, and transaction data, generally represented as a *Merkle tree*. 

The timestamp proves that the transaction data existed when the block was published to get into its hash. This structure allows for the data structure to be immutable, and provides a linear forward history.
