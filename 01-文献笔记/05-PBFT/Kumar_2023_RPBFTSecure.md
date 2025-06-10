Kumar\_2023\_RPBFTSecure
Title:: R-PBFT: A secure and intelligent consensus algorithm for internet of vehicles
Citekey:: Kumar\_2023\_RPBFTSecure
Author:: Amritesh Kumar; Lokendra Vishwakarma; Debasis Das
Date:: 2023-06-01
Journal:: Vehicular Communications
Tags:: #PBFT  #主节点选择优化  #信誉机制  #逻辑回归模型
File:: [Kumar 等\_2023\_R-PBFT A secure and intelligent consensus algorithm.pdf](zotero://open-pdf/0_WNKA6CDE)
Work:: 提出了一种称为R-PBFT（Reputed PBFT）的快速智能共识机制，利用逻辑回归计算节点的声誉值来选举领导者和验证节点。
## 研究背景
随着车联网（Internet of Vehicles, IoV）技术的发展，保障数据完整性、不可篡改性及安全性变得尤为重要。传统的车联网采用中心化网络架构，易受单点故障和性能瓶颈的影响。此外，现有的共识算法如PBFT和PoW虽提高了通信和存储效率，但仍存在共识延迟长、交易频率低和区块拥塞等限制。
## 研究目的
针对现有技术的局限，本研究提出了一种称为R-PBFT（Reputed PBFT）的快速智能共识机制，旨在通过引入声誉机制改进PBFT共识过程，以减少共识延迟，提高交易频率和吞吐量，减少区块拥塞，并增强公平性。
## 研究技术
R-PBFT机制利用逻辑回归计算节点的声誉值来选举领导者和验证节点。通过优化PBFT过程，降低了通信和存储的资源需求，同时提高了系统的安全性和效率
## 研究内容
### **声誉值计算**
#### 恶意率
评估IoV对象可能进行恶意行为的概率
α表示IoV对象在N次消息中发送错误消息的次数
公式为：
![\<img alt="" data-attachment-key="I4PKLJ2N" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FWNKA6CDE%22%2C%22annotationKey%22%3A%22SNQFEMQI%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226%22%2C%22position%22%3A%7B%22pageIndex%22%3A5%2C%22rects%22%3A%5B%5B43.367%2C264.222%2C81.17%2C288.416%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FTFLH88UE%22%5D%2C%22locator%22%3A%226%22%7D%7D" width="63" height="40" src="05-附件/I4PKLJ2N.png" ztype="zimage">](05-附件/I4PKLJ2N.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FTFLH88UE%22%5D%2C%22locator%22%3A%226%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/TFLH88UE">Kumar 等, 2023, p. 6</a></span>)</span>
#### 推荐值（REE）
基于其他IoV对象对该对象的正面或负面评价的比例
Pv：支持该消息的投票数
Nv：反对该消息的投票数
公式为：
![\<img alt="" data-attachment-key="Q8AQ2N9Y" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FWNKA6CDE%22%2C%22annotationKey%22%3A%22ZQP8ERXE%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226%22%2C%22position%22%3A%7B%22pageIndex%22%3A5%2C%22rects%22%3A%5B%5B44.375%2C143.083%2C112.421%2C171.31%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FTFLH88UE%22%5D%2C%22locator%22%3A%226%22%7D%7D" width="113" height="47" src="05-附件/Q8AQ2N9Y.png" ztype="zimage">](05-附件/Q8AQ2N9Y.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FTFLH88UE%22%5D%2C%22locator%22%3A%226%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/TFLH88UE">Kumar 等, 2023, p. 6</a></span>)</span>
#### 逻辑回归模型
综合考虑上述因素来计算最终的声誉值（RPv）。
A：包含恶意率（Mr）、推荐值（REE）、以及历史声誉值（RPv-1）的特征向量。
B：通过线性最小二乘法评估的权重向量。
C：用于调整初始声誉值的偏置值。
公式为：
![\<img alt="" data-attachment-key="37JWFJ4Z" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FWNKA6CDE%22%2C%22annotationKey%22%3A%224YLSFG8M%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%226%22%2C%22position%22%3A%7B%22pageIndex%22%3A5%2C%22rects%22%3A%5B%5B45.887%2C87.135%2C129.055%2C112.337%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FTFLH88UE%22%5D%2C%22locator%22%3A%226%22%7D%7D" width="139" height="42" src="05-附件/37JWFJ4Z.png" ztype="zimage">](05-附件/37JWFJ4Z.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FTFLH88UE%22%5D%2C%22locator%22%3A%226%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/TFLH88UE">Kumar 等, 2023, p. 6</a></span>)</span>
### **共识过程**
#### a. 领导者和验证者的选举
基于节点的声誉值，选择声誉最高的节点作为领导者（Leader），负责提议新的区块。声誉值大于某一阈值的其他节点被选为次级验证者（Secondary Validators），参与区块的验证过程。
#### b. 区块的提议和验证
领导者节点提出新的区块，并将其广播给所有次级验证者。次级验证者对区块进行验证，验证过程中如果超过三分之二的验证者同意该区块的有效性，区块则被确认并添加到区块链中。
## 实验结果
结果显示R-PBFT在减少共识延迟（50%）、提高交易频率（24%）、增加吞吐量（50%）、减少区块拥塞（57%）及提升公平性（15%）方面均优于现有技术。
## 未来与展望
未来研究将探讨如何进一步优化共识机制以适应更大规模的网络，同时增强系统对多种网络攻击的抵抗能力，如Sybil攻击和Eclipse攻击。此外，也将研究如何在不牺牲安全性的前提下进一步提升系统的性能和效率。
