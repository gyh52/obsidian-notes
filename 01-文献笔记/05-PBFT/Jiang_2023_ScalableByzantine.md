Jiang\_2023\_ScalableByzantine
Title:: A scalable byzantine fault tolerance algorithm based on a tree topology network
Citekey:: Jiang\_2023\_ScalableByzantine
Author:: Wangxi Jiang; Xiaoxiong Wu; Mingyang Song; Jiwei Qin; Zhenhong Jia
Date:: 2023-04-03
Journal:: IEEE Access
Tags:: #PBFT  #树型拓扑 #局部共识 #其他共识优化 #多层共识 
File:: [Jiang 等\_2023\_A Scalable Byzantine Fault Tolerance Algorithm Based on a Tr.pdf](zotero://open-pdf/0_76SFYWNS)
Work:: STBFT算法基于树形拓扑网络，将全局共识转变为局部共识，通过不同层级和分组共识节点减少通信消耗。采用了可验证随机函数（VRF）来防止拜占庭节点的集中和串通，增强了系统的安全性。利用反馈机制用于监控和中继节点行为，减少拜占庭故障对系统的影响。
## 研究背景
传统的实用拜占庭容错（PBFT）算法适用于小规模局域网络，但在大规模广域网络环境中，由于其可扩展性瓶颈，会严重影响系统性能。随着应用场景的扩大，如物联网和医疗保健领域，对于能在大规模网络中有效运作的拜占庭容错算法的需求日益增加。
## 研究目的
本研究旨在提出一种新的基于树形拓扑网络结构的拜占庭容错算法，以解决传统PBFT算法在大规模网络环境中的可扩展性问题，并通过减少通信消耗、防止有针对性攻击以及增强系统容错性能，提高算法的应用性。
## 研究技术
STBFT算法基于树形拓扑网络，将全局共识转变为局部共识，通过不同层级和分组共识节点减少通信消耗。采用了可验证随机函数（VRF）来防止拜占庭节点的集中和串通，增强了系统的安全性。利用反馈机制用于监控和中继节点行为，减少拜占庭故障对系统的影响。
## 研究内容
### 系统模型
树形网络拓扑易于扩展且可以有效隔离故障。所有的网络节点被分层次地组织起来，形成不同的区域，整个网络的共识被分解为多个子网的局部共识。
![\<img alt="" data-attachment-key="G6HJ95P3" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F76SFYWNS%22%2C%22annotationKey%22%3A%22Y8DIXJA5%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%2233512%22%2C%22position%22%3A%7B%22pageIndex%22%3A3%2C%22rects%22%3A%5B%5B325.392%2C533.63%2C510.727%2C720.427%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FYENTYEUT%22%5D%2C%22locator%22%3A%2233512%22%7D%7D" width="309" height="311" src="05-附件/G6HJ95P3.png" ztype="zimage">](05-附件/G6HJ95P3.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FYENTYEUT%22%5D%2C%22locator%22%3A%2233512%22%2C%22label%22%3A%22page%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/YENTYEUT">Jiang 等, 2023, page 33512</a></span>)</span>
共识域：每个父节点（非叶节点）与其子节点一起形成一个子网络
每层的主节点不参与其子节点的共识，仅负责发送请求消息并收集投票结果。
### 共识过程
预准备阶段：每个节点接收来自父节点的请求，通过多播发送预准备消息给同一共识域内的其他节点。
准备阶段：节点收到有效的预准备消息后，进入准备阶段，并向同域节点多播准备消息。
提交阶段：如果一个节点收到超过2/3的匹配准备消息，该节点进入提交阶段。
回复：提交阶段成功后，节点生成一个证书，向其父节点发送回复消息。
### 随机分组策略
为了防止拜占庭节点的集中和串通，STBFT引入了基于可验证随机函数（VRF）的随机分组策略。
确保每个节点的分组是随机且不可预测的，增加了系统的安全性。
每个节点使用VRF生成一个伪随机数，根据这个数值被分配到相应的组中。这个分组信息由一个集中的GST中心维护，但不参与任何共识决策，仅用于信息存储和验证。
### 反馈机制
反馈机制用于监控和中继节点行为，减少拜占庭故障对系统的影响。
当节点展示出拜占庭行为时，反馈机制可以激活，允许系统在不同的层次间进行错误校正和数据同步，提高算法的容错性。
## 实验结果
通过仿真实验，证明了STBFT算法相较于传统PBFT算法，在通信复杂性和系统容错性能方面有显著提升。
实验结果显示，STBFT算法能在保持高容错性的同时，显著降低通信开销，并能更好地适用于大规模场景。
## 未来与展望
尽管STBFT算法在多个方面展示了优势，但对于系统中故障节点数量的容忍度仍有限。未来研究将致力于解决层级系统中的延迟和容错问题，以便联盟链可以应用于更严苛和复杂的环境中。
