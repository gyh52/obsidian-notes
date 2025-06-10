Xu\_2021\_EfficientBlockchain
Title:: An efficient blockchain PBFT consensus protocol in energy constrained IoT applications
Citekey:: Xu\_2021\_EfficientBlockchain
Author:: Xiaoqiong Xu; Gang Sun; Hongfang Yu
Date:: 2021-11-04
Journal:: 2021 International Conference on UK-China Emerging Technologies (UCET)
Tags:: #PBFT #能源受限  #选择节点优化   #主节点选择优化
File:: [Xu 等\_2021\_An Efficient Blockchain PBFT Consensus Protocol in Energy Co.pdf](zotero://open-pdf/0_BVBGG7D2)
Work:: 提出一种针对能源受限的物联网区块链应用的高能效拜占庭容错（PBFT）共识协议。根据节点的可用能量作为阈值构建共识节点组。使用了可验证随机函数（VRF）来确保领导者的安全性，并通过扩展中心性度量来选择中继节点，以此优化多跳邻居节点情况下的节点权限管理。
## 研究背景
在物联网（IoT）领域中，尽管能够支持各种智能应用，数据隐私和安全问题仍然存在，这是由于物联网设备的多样性所引起的。区块链技术以其分布式、可追溯和不可篡改的特性，提供了解决这些问题的可能性。然而，由于物联网设备的能源和计算能力限制，传统的工作量证明（PoW）基础的区块链系统中的共识机制显得过于昂贵且效率低下。
## 研究目的
本文旨在提出一种针对能源受限的物联网区块链应用的高能效拜占庭容错（PBFT）共识协议，旨在降低能源消耗并提高系统性能。
## 研究技术
文章中提出的协议使用了可验证随机函数（VRF）来确保领导者的安全性，并通过扩展中心性度量来选择中继节点，以此优化多跳邻居节点情况下的节点权限管理。
## 研究内容
*   **能效共识节点选择机制**：根据节点的可用能量作为阈值构建共识节点组。
*   **安全领导者选择**：应用VRF，以随机和验证的方式选举领导者，确保选举结果的不可预测性。
*   **优化的消息传输**：采用gossip协议和基于“closeness”中心性的节点选择，减少通信复杂度和提高消息传播效率。
## 实验结果
模拟实验结果验证了所提共识协议能显著降低能源消耗，并在节点数量增多时仍能保持较高的性能表现。此外，相较于传统PBFT协议，改进的协议在安全性和攻击抵抗能力方面表现更佳。
## 未来与展望
研究指出虽然新的共识协议在能源效率和性能上有显著改进，但仍需进一步研究如何在更广泛的应用场景中实现和优化这些技术。此外，还需探讨如何进一步降低因节点增多导致的延迟问题，并提高系统的可扩展性和可靠性。
