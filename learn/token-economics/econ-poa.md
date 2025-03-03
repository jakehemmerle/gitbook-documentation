# Proof of Authority

### Mainnet

Dock launched its mainnet in September 2020 with 11 independent validators running the network with a Proof of Authority \(PoA\) consensus. The validators were the top performers selected during the PoA testnet phase and were selected based on a variety of criteria to ensure network diversity and optimal performance. Applicants were required to join share their details for KYC \(Know Your Customer\) and public keys.

#### **Key points:**

* The network has 11 validators.
* Time is divided into intervals of 10 days and each interval is called an epoch.
* The network rewards validators for participating in block production and each validator will get an equal opportunity to produce blocks.
* As an additional reward, the validators get to keep 100% of the fees of any transactions they process in a block.
* 50% of the block rewards received by the validator during the PoA network are locked until the launch of the PoS network. Once the PoS network is launched, the locked rewards will be released gradually \(more on that below\).
* Any malicious behavior by a validator will lead to immediate disqualification and prohibition from participating in the network and may prevent any future participation.

#### **Description**

Network validators are selected by the network in a round-robin fashion to produce blocks such that each validator gets an equal opportunity to produce blocks in an epoch. However, the actual rewards received by the validator depend on the availability of the validator which, in turn, depends on the number of blocks they produce. The network is only guaranteeing equal opportunity to validators, but not guaranteeing equal rewards. 

During each epoch, the network will offer 15K Dock tokens to each validator, thus the network \(with 10 validators\) will offer 150K Dock tokens in total to all validators. If a validator is fully available, i.e. it produces all the blocks that it can, it will get 15K tokens in the epoch which equates to 45K tokens per month. However, if the validator is unavailable for some time \(the node crashed, the network was down or some other reason\), they should expect a proportionate loss of rewards.

_block rewards in an epoch_ = `r`   
_block produced in the epoch_ = `b`   
_blocks that could be produced in the epoch_ = `B`   
_maximum block rewards in the epoch per validator_ = `p`

```text
r = (b / B) * p
```

E.g. if a validator could produce 100 blocks in an epoch but only produced 75 blocks, its rewards will be 11.25K = \(.75\*15K\).

As the Dock Association is responsible for the ongoing development, governance, management, and marketing of the network, 60% of the total block rewards released will go to the Dock Treasury. To keep validators invested in the long term, 50% of the block rewards of each validator are locked up until the PoS network is launched. On the launch of the PoS network, the 1st epoch will release locked funds of all validators earned in the 1st epoch of the PoA network, the 2nd epoch of PoS will release locked funds of the 2nd epoch of the PoA network and so on. Thus, a validator earning 15K tokens in say the 10th epoch of PoA network has 7.5K tokens locked in the network which are released in the 10th epoch of the PoS network. 

Validators have one more revenue stream; the fees of the transactions they process. Any fees for transactions processed by a validator are immediately credited towards the validator's account and neither are locked nor influence the rewards of the Dock Treasury.

This PoA testnet will transition into the PoS testnet for development and testing prior to launching the PoS mainnet.



