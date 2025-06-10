Kim\_2023\_ByzantinefaulttolerantConsensus
Title:: Byzantine-fault-tolerant consensus via reinforcement learning for permissioned blockchain-empowered V2X network
Citekey:: Kim\_2023\_ByzantinefaulttolerantConsensus
Author:: Seungmo Kim; Ahmed S. Ibrahim
Date:: 2023-01
Journal:: IEEE Transactions on Intelligent Vehicles
Tags:: #强化学习 #PBFT #选择节点优化 #TS算法 #MAB
File:: [9760010.html](zotero://open-pdf/0_KBPJ8IX7)
Work::  通过强化学习（RL）机制，使用情景多臂老虎机模型和Thompson Sampling算法，动态优化参与共识过程的节点数量。
## 研究背景
本文探讨了区块链技术在车联网（V2X）中的应用，特别是许可区块链在提高可扩展性和满足不同组织需求方面的优势。研究的重点是优化许可区块链中参与共识过程的节点数量，尤其在节点因移动性导致网络动态变化的V2X网络中。
## 研究目的
本文旨在通过强化学习（RL）优化许可区块链（特别是Hyperledger Fabric）在V2X网络中的共识机制，确保在动态变化的网络环境中实现最佳的节点选择，从而平衡节点数量与网络可扩展性和容错性的关系。
## 研究技术
研究采用强化学习（RL）方法，将问题建模为情景多臂老虎机（contextual multi-armed bandit, MAB）问题。
## 研究内容
**共识节点选择**：通过强化学习（RL）机制，使用情景多臂老虎机模型和Thompson Sampling算法，动态优化共识节点选择。
1.  **强化学习机制**：
    *   车辆在进入网络之前进行训练，学习不同情境下的节点选择策略。
    *   使用Thompson Sampling（TS）算法来解决探索
    *   利用困境，通过不断更新奖励分布来选择最优节点。
2.  **多臂老虎机模型（MAB）**：
    *   每辆车根据当前的上下文信息（如停留时间、节点故障概率等）选择一组节点进行共识。
    *   使用Beta-Bernoulli分布来建模奖励，即一个交易成功执行并在停留时间内被提交。
3.  **节点选择过程**：
    *   车辆在进入网络时，发送加入请求并接收包含网络信息的确认消息。
    *   根据接收到的信息，车辆在训练期内观察并更新不同通道的奖励分布。
    *   训练期结束后，车辆使用已学习的奖励分布来选择最优通道（节点组合）进行交易提议。
**领导节点选择**：本文基于Hyperledger Fabric采用Raft协议进行领导节点选举，Raft协议本身通过动态选举领导者节点确保了系统的稳定性和可靠性。
## 实验结果
提出的RL机制在延迟和吞吐量方面表现优于现有方法。
在不同节点数量和故障概率条件下，优化机制能够显著降低延迟，提高网络的可扩展性。
TS算法在选择最优通道时表现出较好的收敛性和稳定性。
## 未来与展望
将RL机制应用于其他动态因素（如网络条件）的优化。
探讨其他Hyperledger区块链在V2X网络中的可行性。
进一步改进算法，提高在实际应用中的适应性和鲁棒性。
