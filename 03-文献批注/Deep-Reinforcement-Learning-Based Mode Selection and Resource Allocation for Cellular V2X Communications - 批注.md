 Mdnotes File Name: [[Zhang_2020_DeepReinforcementLearningBasedMode]]

# 工作
考虑到局部DRL模型的训练限制，提出了一种两时间尺度的联邦DRL算法以获得鲁棒的模型：
1.  基于图论的车辆聚类算法在大时间尺度上执行
2.  联邦学习算法在小时间尺度上执行
![[Pasted image 20230514175418.png|500]]
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FWT8IDNY9%22%5D%2C%22locator%22%3A%226386%22%7D%5D%2C%22properties%22%3A%7B%7D%7D">(<span class="citation-item">Zhang 等, 2020, p. 6386</span>)</span>

仿真结果表明，所提出的基于DRL的算法优于其他去中心化基线，验证了新激活V2V对的双时间尺度联合DRL算法的优越性。

# 联邦学习
## 概念
现有的数据计算和模型训练大多在集中式服务器或计算机集群中进行。由于隐私和通信成本问题，大多数设备不愿意共享私有数据。另一方面，设备端局部数据的模型训练和数据分析往往耗时且不精确。为了应对这些挑战，联邦学习被提出，允许参与设备在中央服务器的协调下进行松散的联合。

## 优点
1.  在设备端利用基于本地原始数据的本地训练
2.  在集中式服务器上对本地模型进行非频繁平均