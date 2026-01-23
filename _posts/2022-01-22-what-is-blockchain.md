---
layout: default
title: "What is blockchain"
tags: blockchain
---

# <a name="top"></a>Blockchain - the basics

## **1. Blockchain in short**

A blockchain is a **digital chain of blocks**:

* Each **block** contains:

  1. Transactions or data (for example, who sends money to whom)
  2. A **hash** of its own block
  3. The **hash of the previous block**

* **Why this matters:** It ensures that every block is **linked to the previous one**, and that the chain **cannot be changed** without it being noticed.

## **2. What is a hash?**

* A **hash** is a unique digital code that is calculated from the contents of a block.
* Think of it as a **fingerprint of the block**: if you change even the smallest detail in the block, the hash changes completely.
* This is how the network knows: “Hey, this block was changed — something is wrong!”

**Analogy:**

* You write a letter and seal it with a special stamp (the hash).
* If someone changes the letter, the seal no longer matches. Everyone can immediately see that it’s been tampered with.

## **3. How blocks are linked together**

* Each block contains **the hash of the previous block**.
* So if someone tries to change an old block:

  1. The hash of that block changes.
  2. The following blocks no longer match, because their “previous hash” is no longer correct.
* This makes **fraud almost impossible**.

**Visualization:**

```
[Block 1] → [Block 2] → [Block 3] → [Block 4]
   ^           ^           ^
 previous    previous    previous
  hash        hash        hash
```

## **4. How consensus mechanisms (PoW / PoS) fit into this**

* **Proof of Work (PoW)**: Computers must solve a difficult puzzle to add a new block. This proves that the block is legitimate.
* **Proof of Stake (PoS)**: People with more coins are selected to add new blocks.
* **Result:** Only blocks that are **valid and approved by the network** are added to the chain.

## **5. Security summary**

* **Hashing** = every block is unique and cannot be changed unnoticed
* **Previous hash** = blocks form a chain → changing one block breaks everything after it
* **Consensus mechanism** = the network decides who may add a new block → prevents cheating

💡 **Short example:**

* Block 1 → hash: ABC
* Block 2 → hash of its own content + reference to ABC
* Block 3 → hash of its own content + reference to the hash of Block 2
* Try to change Block 2, and Block 3 no longer matches → everyone sees it immediately.
