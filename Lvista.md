---
timezone: Asia/Shanghai
---

# Lvista

1. 自我介绍: 
    - 个人主页：[lvista.site](lvista.site)
    - 个人简介：学生，C，C++，C#，嵌入式，python
2. 你认为你会完成本次残酷学习吗？ 会的。

## Notes

<!-- Content_START -->

TODO: Read https://inevitableeth.com/home/ethereum/world-computer  
TODO: Figuring out the meaning of this [roadmap](https://x.com/VitalikButerin/status/1741190491578810445) or [here](https://ethereum.org/zh/roadmap/)

Links:

| Description  |  Links  |
|---|---|
| Great speech vido | https://archive.devcon.org/archive/ |

### 2025.02.06

今日任务：
- [x] 了解区块链->https://en.wikipedia.org/wiki/Blockchain
- [x] 了解以太坊（Ethereum）的基本要概念->https://epf.wiki/#/eps/week1

#### Block Chain
> See also: [what-is-a-blockchain](https://ethereum.org/zh/developers/docs/intro-to-ethereum/#what-is-a-blockchain)  

以太坊是基于区块链的一种[公有链](https://en.wikipedia.org/wiki/Blockchain#Private_blockchains).

从数据结构上来看，区块链通过首尾相接的“区块”来连接成“链”的，这种链的特点是，
由于每个节点包含前一个结点的信息（Hash Code），每个数据节点的变化会影响后面所有节点，
这样的特点使得数据的变化很容易被发现，从而保证了数据的强壮性。
> See this vido about Blockchain:https://youtu.be/_160oMzblY8

从数据管理方式上来看，区块链是一种分布式帐本，通俗讲就相当于将一个公共帐本拆开，将每一页分给每个帐户，每条交易记录都分布在每个人手上，
这就避免了[双重支出问题](# "甲方帐户扣除一次而在两个乙方帐户上增加")。
没错，就像peer-to-peer (P2P)一样，而Block chain正是由P2P进行管理的。

比如电子人民币就是典型的联盟链的应用。

下面这张表格很好的展示了以太坊的定位:
|          | 公有链                  | 联盟链              | 私有链           |   |   |   |   |   |   |
|----------|----------------------|------------------|---------------|---|---|---|---|---|---|
| **参与者**  | 不限                   | 联盟成员             | 链的所有者         |   |   |   |   |   |   |
| **共识机制** | PoW/PoS              | 分布式一致性算法         | solo/pbft等    |   |   |   |   |   |   |
| **验证者**  | 自愿提供算力或质押加密货币者       | 联盟成员协商确定         | 链的所有者         |   |   |   |   |   |   |
| **激励机制** | 需要                   | 可选               | 无             |   |   |   |   |   |   |
| **去中心化** |                      |                  |               |   |   |   |   |   |   |
| **程度**   | 较高                   | 偏低               | 极低            |   |   |   |   |   |   |
| **如初特点** | 解决双重支付               | 效率和成本优化          | 安全性高、效率高      |   |   |   |   |   |   |
| **吞吐量** | 7笔/秒至数千笔/秒(TPS)      | <10万笔/秒(TPS)     | 视配置决定         |   |   |   |   |   |   |
| **应用领域** | 区块链游戏、非同质化代币、去中心化金融等 | 供应链管理、金融服务、医疗保健等 | 大型组织或私人企业之业务等 |   |   |   |   |   |   |
| **代表项目** | 比特币、以太坊              | R3、 Hyperledger  |               |   |   |   |   |   |   |


#### The Prehistory and Philosophy of Ethereum 
> See also:
> - TODO[Inevitable Ethereum - World Computer](https://inevitableeth.com/home/ethereum/world-computer)
> - TODO[Ethereum in 30 minutes](https://www.youtube.com/watch?v=UihMqcj-cqc)
> - [Ethereum.org docs](https://ethereum.org/zh/what-is-ethereum/)
> - [Ethereum Develop Document](https://ethereum.org/zh/developers/docs/)

以太坊的理念源于类似Unix的免费和开源理念。开放的平台需要安全性，中立性和无信任性,
这成为了以太坊的核心课题。

以太坊的主要高级组成部分是执行层( Execution layer)和共识层(Consensus layer):
- 执行层: Execution layer provides the execution engine, handles user transaction and all state (address, contract data)
> 简而言之就是提供算力
- 共识层: implements the proof-of-stake mechanism ensuring security and [fault tolerance](https://inevitableeth.com/home/concepts/bft)
> 也就是保证数据的健壮，安全，可信

作为区块链的一种，以太坊的[共识机制](https://ethereum.org/zh/developers/docs/consensus-mechanisms/)是[权益证明](https://ethereum.org/zh/developers/docs/consensus-mechanisms/pos/)
> TODO: Lean about the consensus mechanisms

#### 小结
区块链是一种去中心化的公共数据库，相对的中心化数据库就是各种互联网企业。

以太坊是一种公共区块链技术，主要由执行层和共识层构成，
执行层提供执行或者算力，共识层保证以太坊数据的健壮。

### 2025.02.07

#### Implementations and Development
- client and node  
 An implementation of the execution layer (EL) or consensus layer (CL) is called a **client**. A computer running this client and connecting to the network is called a **node**. 

- client diversity  
Ethereum client can be implemented in different language, which make it [diverse](https://ethereum.org/zh/developers/docs/nodes-and-clients/client-diversity/).
[Here is the implementations list](https://ethereum.org/en/developers/docs/nodes-and-clients/#execution-clients).

#### Testing

You can find some test tools from [here](https://epf.wiki/#/eps/week1?id=testing)
#### Coordination

- [PM repo](https://github.com/ethereum/pm)shows the schedule for coordination.
- You can also discuss or propose features through https://ethresear.ch/ or [Ethereum Magicians](https://ethereum-magicians.org/)

#### Bitcoin
> I think [this video](https://youtu.be/eEQ41gD0iC4?si=w5LNr1Va2oM2R0aX) should been seen by everyone who try to develop Ethereum implementations after learning about the basic concept of Ethereum.

Bitcoin is a Cryptocurrency, the transaction of Bitcoin include the following 
factors:
- Signature: To verify the owner of a request, not anyone else, verify the validity of the request.
- Uniqueness: The transaction request is Uni , to avoid the [Dual spending issue] (# "Deducting once from Party A's account and adding to two Party B's accounts")
So the **Proof of Work** comes on stage. 

### 2025.02.08

#### Proof of work (PoW)
> See also: https://youtu.be/_160oMzblY8?si=ySD7m-WXH__b5vlv
and https://youtu.be/eEQ41gD0iC4?si=w5LNr1Va2oM2R0aX

A block of ledger is needed to be proofed for its validity, so making it less likely to be created is a good proof method. 

An block chain is just like this(play it in [here](https://andersbrownworth.com/blockchain/blockchain)):
![block_chain](https://files.catbox.moe/oyxjpg.png)

The hash code below is calculate(or called **Mine**, yes! it is the button below) based on the Data, Nonce, Block, Prev.

- **Data** is the essence
- **Nonce** is the specific num by mining, which makes Hash have multiple zeros starting with it, the more the zeros the greater the workload
- **Prev** is the previous block's Hash, which included into the Mining in current block.
- **Block** is just a num of block index

The "Hash with Zeros" and the Nonce are exactly the Proof of Work.
#### Why is PoW trustworthy

1. Because of the "Chain", once a certain block in the middle is changed, all subsequent blocks will be changed, Moreover, there are many copy of ledger, the forged ledger will be overwhelmed by the correct version.
2. Of cause, the latest block maybe untrustworthy, or perhaps the latest ledger you received was indeed forged by someone else, who mined out in the fastest time. But this won't last long, other miners will soon surpass it, and the ledger will return to its correct state.

#### Proof of stake (PoS)

TODO

#### Gas

Gas is the fee of transaction

**Gas and ETH**  

The unit of gas is *wei*, and Gas prices are usually quoted in *gwei*.
$$
1 gwei =  10^{-9} ETH
$$
**Gas fees calculating**  
$$
Gas\;fees =  units\;of\;gas\;used * (base \;fee + priority\;fee)
$$
- *base fee* is a value set by the protocol, which is finally to be burned and out of currency circulation.
- *priority fee* is a value set by the user as a tip to the validator.

### 2025.02.09
An overview of Week2

> See also: https://ethereum.org/en/developers/docs/nodes-and-clients/

#### Node
> $\mathcal{def}$: A **node** is any instance of Ethereum client software that is connected to other computers also running Ethereum software, forming a network.

**Node type**:  
- light: only download block headers
- full: 
    - Stores full blockchain data (although this is periodically pruned so a full node does not store all state data back to genesis)
    - Participates in block validation, verifies all blocks and states.
    - All states can be either retrieved from local storage or regenerated from 'snapshots' by a full node.
    - Serves the network and provides data on request.
- archive: full nodes that verify every block from genesis and never delete any of the downloaded data.

#### An Overview of the Ethereum Execution Layer
> https://www.youtube.com/watch?v=7sxBjSfmROc

**The Ethereum system**
- The Ethereum System is divided into EL(execution layer Or compute layer) and CL(beacon chain)
- By`notify_new_payload(payload)`, CL do nothing! CL just sends the execution payloads(State updating query) to the EL.
![](https://files.catbox.moe/crd2ea.png)

---
**Ethereum compute layer: the EVM**
> The EVM is just the core of the EL, EL include the [other parts](# "Mempool, State Storage, interface client").
- Two types of accounts:
    - *EOA*: the people's accounts.
    - *contracts*: the "bot".

![](https://files.catbox.moe/dwcric.png)

**Data associated with an account**
![](https://files.catbox.moe/zw9qh7.png)

**Account state: persistent storage**

- Only valid in the *contract*.
- The all data mentioned above is stored as an array(`S[]`)
- These array collectively define the status of the account and are stored in the *Ethereum state tree* through a *Merkle tree* structure.
- *Ethereum state tree* only calc the non-zero cells.

![](https://files.catbox.moe/cq6xbq.png)
### 2025.02.10

<!-- Content_END -->
