Gao\_2019\_TPBFTEigenTrustbased

Title:: T-PBFT: An EigenTrust-based practical byzantine fault tolerance consensus algorithm

Citekey:: Gao\_2019\_TPBFTEigenTrustbased

Author:: Sheng Gao; Tianyu Yu; Jianming Zhu; Wei Cai

Date:: 2019-12

Journal:: China Communications

Tags:: #blockchain , #Blockchain , #Byzantine fault tolerance , #Complexity theory , #Consensus algorithm , #consensus protocol , #Fault tolerance , #Fault tolerant systems , #Probabilistic logic , #Scalability , #trust model

File:: [Gao 等\_2019\_T-PBFT An EigenTrust-based practical Byzantine fault tolera.pdf](zotero://open-pdf/0_TRVT6EMB)

Work:: 提出一种基于EigenTrust模型的优化PBFT共识算法T-PBFT，通过节点信任评估构建高质量共识组，提升拜占庭容错率，用主节点组替代单一主节点，降低视图切换概率，并通过组签名和相互监督增强主节点组的鲁棒性。优化了通信复杂度，提高大规模网络中的共识效率。

## 研究背景

区块链技术因其去中心化、透明可信、时序性和不可篡改等特性被视为一项有前景的技术。共识算法作为区块链的核心技术之一，直接影响系统的可扩展性。现有的共识算法（如PoW、PoS）存在能耗高、效率低的问题，而绝对最终性共识算法（如PBFT、HoneyBadgerBFT）在大规模网络中难以满足可扩展性需求。此外，PBFT等算法依赖单一主节点，主节点故障会触发视图切换（view change），影响共识效率。因此，需要一种更高效、可扩展且容错率高的共识算法。

## 研究目的

提出一种基于EigenTrust模型的优化PBFT共识算法——T-PBFT，旨在：

1.  通过节点信任评估构建高质量共识组，提升拜占庭容错率。
2.  用主节点组（primary group）替代单一主节点，降低视图切换概率。
3.  通过组签名和相互监督增强主节点组的鲁棒性。
4.  优化通信复杂度，提高大规模网络中的共识效率。

## 研究技术

1.  **EigenTrust模型**：通过节点间交易历史计算全局信任值，筛选高信任节点组成共识组。

    *   直接信任值（直接交易节点）和推荐信任值（间接交易节点）结合。
    *   动态更新全局信任值，反映节点行为变化。

2.  **多阶段共识框架**：

    *   **节点信任评估**：基于交易记录计算信任值。
    *   **共识组构建**：选择高信任节点组成共识组。
    *   **共识过程**：主节点组发起预生成区块，通过预准备、准备、回复三阶段达成一致。

3.  **主节点组与组签名**：

    *   主节点组替代单一主节点，降低单点故障风险。
    *   组签名保护成员隐私，防止针对性攻击。

## 研究内容

1.  **节点信任评估**：

    *   使用EigenTrust模型计算节点的直接信任值、推荐信任值和全局信任值（算法1-4）。

2.  **共识组构建**：

    *   按全局信任值排序，选择前d%节点组成共识组（算法5）。
    *   从共识组中选取前m%节点构成主节点组（算法6）。

3.  **共识流程优化**：

    *   **组内监督**：主节点组内部验证预生成区块，避免视图切换。
    *   **三阶段共识**：预准备（广播区块）、准备（验证区块）、回复（客户端确认）。
    *   组签名确保主节点组的匿名性和安全性。

## 实验结果（理论分析）

1.  **拜占庭容错率**：通过信任筛选，共识组中恶意节点比例降低，容错率提升。
2.  **视图切换概率**：主节点组设计减少单点故障，视图切换概率显著降低。
3.  **通信复杂度**：共识组规模缩小，消息复杂度从PBFT的O(n²)优化至O(dn)（d为共识组比例）。
4.  **对比其他BFT算法**：T-PBFT在可扩展性、效率和容错率上优于PBFT、HoneyBadgerBFT等。

## 未来与展望

1.  **动态信任阈值**：探索自适应信任阈值调整策略，优化共识组规模。
2.  **跨链应用**：研究T-PBFT在跨链场景中的兼容性与性能。
3.  **实验验证**：需在实际区块链网络中测试T-PBFT的性能（如吞吐量、延迟）。
4.  **安全增强**：结合零知识证明等密码学技术，进一步提升隐私保护能力。

**总结**：T-PBFT通过EigenTrust模型和主节点组设计，解决了传统BFT算法的可扩展性和视图切换问题，为联盟链提供了一种高效、高容错的共识方案。未来需进一步实验验证并扩展应用场景。
