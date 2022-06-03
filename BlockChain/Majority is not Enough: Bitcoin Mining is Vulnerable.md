# Majority is not Enough: Bitcoin Mining is Vulnerable [Nov, 2013]

### Abstract

Show that bitcoin protocol is not incentive-compatible, colluding miners could obtain a revenue larger than their fair share. Selfish mining and a new bound for mining power (resources).

### Introduction to Selfish Mining

for a pool to keep its discovered blocks private, therefore intentionally forking the chain. This leads honest miners to waste their resources

<img src="/Users/bettywu/Library/Application Support/typora-user-images/截屏2022-06-03 16.33.59.png" alt="截屏2022-06-03 16.33.59" style="zoom:50%;" />

### Analysis of Selfish-Mine

Use a state machine to analyze the system. Assuming the mining power of the selfish pool and honest pool are $\alpha$ and $1-\alpha$, respectively. $\gamma$ is the ratio of honest miners that choose to mine on the selfish block when the lengths of two chains are equal.

The states of the system represent the lead of the selfish pool; that is, the difference between the number of unpublished blocks in the pool’s private branch and the length of the public branch.

<img src="/Users/bettywu/Library/Application Support/typora-user-images/截屏2022-06-03 16.37.19.png" alt="截屏2022-06-03 16.37.19" style="zoom:50%;" />

<img src="/Users/bettywu/Library/Application Support/typora-user-images/截屏2022-06-03 16.40.43.png" alt="截屏2022-06-03 16.40.43" style="zoom:33%;" />

We further show that the upper bound on threshold size is 1/3: the protocol will never be safe against attacks by a selfish mining pool that commands more than 33% of the total mining power of the network

<img src="/Users/bettywu/Desktop/同步文件夹/Paper-Reading/BlockChain/pics/截屏2022-06-03 19.12.37.png" alt="截屏2022-06-03 19.12.37" style="zoom:33%;" />

When this is larger than $\alpha$ , selfish mining is profitable, thus leading to<img src="/Users/bettywu/Desktop/同步文件夹/Paper-Reading/BlockChain/pics/截屏2022-06-03 19.13.43.png" alt="截屏2022-06-03 19.13.43" style="zoom:33%;" />

offering the upper bound $\alpha $= 1/3, if alpha is larger than 1/3, then selfish mining will always be incentive

### Solution

suggest a simple modification to the Bitcoin protocol that achieves a threshold of 1/4: Specifically, when a miner learns of competing branches of the same length, it should propagate all of them, and choose which one to mine on uniformly at random. 