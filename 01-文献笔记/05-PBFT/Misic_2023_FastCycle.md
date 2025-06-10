Misic\_2023\_FastCycle
Title:: Fast cycle multiple entry PBFT consensus
Citekey:: Misic\_2023\_FastCycle
Author:: Jelena Mišić; Vojislav B. Mišić; Elham Amini; Zahra Mohtajollah; Xiaolin Chang
Date:: 2023-05-28
Journal:: ICC 2023 - IEEE International Conference on Communications
Tags:: #PBFT  #多领导节点  #快速循环 #马尔可夫决策 #主节点选择优化  #其他共识优化 
File:: [Mišić 等\_2023\_Fast Cycle Multiple Entry PBFT Consensus.pdf](zotero://open-pdf/0_796DVQMW)
Work:: 传统PBFT算法在处理多个提案时，依赖于单一领导节点，且在高负载下表现不佳。本文提出一种改进的方案，通过多个领导节点同时提出区块提案，并在收集阶段，引入快速循环，采用马尔可夫链模型和排队理论模型。
## 研究背景
PBFT在容忍拜占庭错误方面表现出色，但其在物联网应用中存在单个领导节点依赖性和延迟问题。为了提高PBFT在高负载下的性能，已有研究提出了多入口和领导轮换机制​​。
## 研究目的
本研究旨在扩展先前描述的多入口PBFT版本，引入快速循环能力，以通过简化的共识循环处理多个数据块提案，从而提高共识性能，特别是在高流量负载下​​。
## 研究技术
传统PBFT算法在处理多个提案时，依赖于单一领导节点，且在高负载下表现不佳。本文提出一种改进的方案，通过多个领导节点同时提出区块提案，并在收集阶段，引入快速循环，采用马尔可夫链模型和排队理论模型。
## 研究内容
### 确定领导节点和提案的流程
![\<img alt="" data-attachment-key="SMY4GDPD" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F796DVQMW%22%2C%22annotationKey%22%3A%227SFRLF52%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%223659%22%2C%22position%22%3A%7B%22pageIndex%22%3A1%2C%22rects%22%3A%5B%5B147.775%2C624.283%2C461.807%2C720.669%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FJSDQPDQ4%22%5D%2C%22locator%22%3A%223659%22%7D%7D" width="523" height="161" src="05-附件/SMY4GDPD.png" ztype="zimage">](05-附件/SMY4GDPD.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FJSDQPDQ4%22%5D%2C%22locator%22%3A%222%22%2C%22label%22%3A%22page%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/JSDQPDQ4">Mišić 等, 2023, page 2</a></span>)</span>
#### 1. 预备阶段（Pre-Prepare Phase）
在预备阶段，系统中的所有副本节点（replicas）都有机会提出区块提案（block proposals）。
#### 2. 提案提交（Proposal Submission）
所有副本节点都作为潜在的领导节点，通过PREPREPARE消息广播给其他副本节点，提交认为应该包含在区块链中的交易。
#### 3. 收集阶段（Collection Phase）
副本节点进入“脆弱期”（vulnerable period），接收来自多个领导节点的提案。目的：收集尽可能多的提案，在后续阶段进行排序和处理。
#### 4. 提案排序与处理（Proposal Sorting and Processing）
所有提案按照哈希值排序，排序后依次进入PREPARE和COMMIT阶段共识，确保超过2/3的副本节点同意某个提案。最终确定领导节点和被接受的提案。
### 模型
#### 马尔可夫链模型
**状态转移**：每个节点在不同状态之间的转移由马尔可夫链描述。节点的提案到达率相同，区块大小恒定，传输时间为固定值。
#### 排队理论模型
**系统时间分布**：使用排队理论分析系统在不同负载下的表现。重点分析收集阶段和准备/提交阶段的时间分布和总系统时间。
**周期时间的推导**：通过拉普拉斯变换求解系统周期时间和等待时间的分布。
## 实验
### 实验指标
平均周期时间（Mean Cycle Time）：分析不同节点数和提案到达率下的平均周期时间。
周期时间的变异系数（Coefficient of Variation of Cycle Time）：评估系统在不同负载下的稳定性。
### 实验结果
低负载性能：在低负载情况下，提案争用较少，系统性能接近传统PBFT。
高负载性能：在高负载情况下，多个提案批量处理，系统性能显著优于传统PBFT。
## 未来与展望
未来研究方向包括进一步优化快速循环多入口PBFT方案，以适应更大规模的物联网系统，并探索其在其他分布式系统中的应用潜力。此外，还可以研究如何在不牺牲故障容忍率的情况下进一步提高性能​​。
