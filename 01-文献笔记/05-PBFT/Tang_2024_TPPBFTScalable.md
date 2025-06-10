Tang\_2024\_TPPBFTScalable
Title:: TP-PBFT: A scalable PBFT based on threshold proxy signature for IoT-blockchain applications
Citekey:: Tang\_2024\_TPPBFTScalable
Author:: Fei Tang; Tingxian Xu; Jinlan Peng; Ning Gan
Date:: 2024-05-01
Journal:: IEEE Internet of Things Journal
Tags:: #PBFT  #选择节点优化  #信誉机制
File:: [Tang 等\_2024\_TP-PBFT A Scalable PBFT Based on Threshold Proxy Signature.pdf](zotero://open-pdf/0_WJA54XMB)
Work:: 本文旨在设计一种新的阈值代理签名方案，使代理签名者能够代表离线节点签署消息，并通过“两步聚类”方法构建双层架构，以提高PBFT的可扩展性。引入信誉机制来评估节点的质量。
## 研究背景
随着物联网（IoT）和区块链技术的融合应用，确保这些不可信设备之间数据的一致性变得尤为重要。实用拜占庭容错（PBFT）作为一种典型的共识算法，因其计算复杂度低、执行成本低和延迟低等优势，被认为非常适合于物联网区块链应用。然而，PBFT在节点扩展性和离线容错方面存在限制，当超过三分之一的节点离线时，系统将崩溃。这种情况在物联网场景中经常发生，严重限制了物联网区块链网络的安全性和稳定性。为了解决上述问题，本文提出了一种基于阈值代理签名的可扩展PBFT共识协议（TP-PBFT），以提高PBFT在物联网区块链应用中的可扩展性和离线容忍度。
## 研究目的
本文旨在设计一种新的阈值代理签名方案，使代理签名者能够代表离线节点签署消息，并通过“两步聚类”方法构建双层架构，以提高PBFT的可扩展性。此外，引入信誉机制来评估节点的质量。实验结果表明，TP-PBFT共识协议在离线节点超过三分之一的情况下也能达成共识。
## 研究技术
1.  **阈值代理签名**：设计了一种新的阈值代理签名方案，使代理签名者能够代表离线节点签署消息。
2.  **两步聚类方法**：通过两步聚类方法构建双层架构，提高共识算法的可扩展性。
3.  **信誉机制**：引入信誉机制评估节点质量，逐步清除拜占庭节点或不活跃节点。
## 研究内容
### 阈值代理签名
用于解决超过三分之一的节点离线时系统无法达成共识的问题。
基本思想: 将签名权授权给多个代理签名者，使得即使部分节点离线，代理签名者也能代表这些离线节点签署消息，维持系统的正常运行。
### 两步聚类算法
1.  **第一步聚类**：选择信誉值最高的n1个节点作为聚类中心，通过K-Medoids算法对所有节点进行初始聚类，使每个节点选择最近的聚类中心加入对应的聚类。
2.  **第二步聚类**：在初始聚类基础上，进一步聚类形成多代表点（RPs）的集群。每个集群由多个代表点描述，两个最接近的聚类进行聚合操作，直至每个集群的代表点数量达到λ。
### 信誉机制
1.  **初始化**：
    *   每个节点在注册时都会被赋予一个初始信誉值（通常为0.5）。
2.  **评估指标**：
	- **未完成率（θ）**：节点未完成共识的次数/参与共识总次数
	- **恶意率（ξ）**：节点发送错误消息的次数/参与共识总次数
	- **活跃率（φ）**：衡量节点在线时间、网络延迟和加入网络的时间比例
	- φi = (δi + li)/Ti∈ (0, 1]<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F7DJ6566C%22%5D%2C%22locator%22%3A%2215438%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/7DJ6566C">Tang 等, 2024, p. 15438</a></span>)</span>
	- **交易量因子（ψ）**：衡量节点历史交易处理能力
	![\<img alt="" data-attachment-key="MIQZYYP5" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FWJA54XMB%22%2C%22annotationKey%22%3A%22MGMZDBMU%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%2215439%22%2C%22position%22%3A%7B%22pageIndex%22%3A5%2C%22rects%22%3A%5B%5B130.674%2C667.847%2C232.76%2C697.903%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F7DJ6566C%22%5D%2C%22locator%22%3A%2215439%22%7D%7D" width="170" height="50" src="05-附件/MIQZYYP5.png" ztype="zimage">](05-附件/MIQZYYP5.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F7DJ6566C%22%5D%2C%22locator%22%3A%2215439%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/7DJ6566C">Tang 等, 2024, p. 15439</a></span>)</span>
3.  **信誉值计算**：
![\<img alt="" data-attachment-key="92H45QNV" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FWJA54XMB%22%2C%22annotationKey%22%3A%22PCJ9K65A%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%2215439%22%2C%22position%22%3A%7B%22pageIndex%22%3A5%2C%22rects%22%3A%5B%5B79.372%2C536.223%2C261.78%2C553.323%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F7DJ6566C%22%5D%2C%22locator%22%3A%2215439%22%7D%7D" width="304" height="28" src="05-附件/92H45QNV.png" ztype="zimage">](05-附件/92H45QNV.png)\
    <span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F7DJ6566C%22%5D%2C%22locator%22%3A%2215439%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/7DJ6566C">Tang 等, 2024, p. 15439</a></span>)</span>
4.  **信誉值更新**：
    *   每轮共识结束后，根据节点在共识过程中的表现更新其信誉值。如果节点的信誉值低于阈值（如0.5），则该节点将被移出共识组，新的节点或信誉值高于阈值的节点将被加入共识组。
5.  **信誉增长率**：
    *   为了增强节点的稳定性和容错性，引入信誉增长率（R）。信誉增长率用于衡量节点在多个共识轮次中的信誉变化情况。
![\<img alt="" data-attachment-key="JIJ7EBVK" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FWJA54XMB%22%2C%22annotationKey%22%3A%22RYEMMAWC%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%2215439%22%2C%22position%22%3A%7B%22pageIndex%22%3A5%2C%22rects%22%3A%5B%5B93.363%2C423.254%2C249.343%2C457.456%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F7DJ6566C%22%5D%2C%22locator%22%3A%2215439%22%7D%7D" width="260" height="57" src="05-附件/JIJ7EBVK.png" ztype="zimage">](05-附件/JIJ7EBVK.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F7DJ6566C%22%5D%2C%22locator%22%3A%2215439%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/7DJ6566C">Tang 等, 2024, p. 15439</a></span>)</span>
## 实验结果
1.  **阈值代理签名分析**：TP-SM2与原始SM2签名的效率基本相同，表明阈值代理签名的引入并未显著影响签名效率。
2.  **通信开销分析**：与传统PBFT相比，TP-PBFT显著减少了通信次数，尤其在节点量增加的情况下更为明显。实验数据验证了TP-PBFT在通信开销上的优势。
## 未来与展望
1.  **实际设备实验**：在实际物联网设备上实现和测试TP-PBFT协议，进一步验证其在真实环境中的性能。
2.  **算法优化**：根据实验反馈进一步优化TP-PBFT协议，提高其在高节点数量和高延迟网络中的适应性。
3.  **扩展应用场景**：探索TP-PBFT协议在其他动态网络环境中的应用，如智能交通、智能家居等领域。
