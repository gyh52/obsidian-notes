 Mdnotes File Name: [[Li_2021_DeepReinforcement]]

# 批注

批注

摘要

为了提高频谱资源的利用率，

本文研究了正交频分复用( OFDM )技术下的资源块( RB )共享和车辆传输功率分配问题。

1.  为了满足车-路( V2I )链路的高数据速率和车-车( V2V )链路的高可靠性，优化问题被定义为最大化一个加权效用函数，该函数可以联合表示两类V2X链路的不同需求。
2.  考虑到车辆环境的高移动性，我们提出了在线分布式多智能体强化学习( MARL )方法来解决上述非凸优化问题，并设计了强化学习的三要素。

背景

传统方法很难解决日益密集和异构网络中的问题。此外，车载环境下的快时变信道使得中央控制器难以收集准确的信道状态信息( CSI )，给资源分配问题带来挑战。基于以上分析，本文将每条V2V链路建模为一个智能体，并提出了一种基于DRL的资源分配策略，即多智能体强化学习( Multi-Agent Reinforced Learning，MARL )，以自适应地配置频谱和车辆传输功率。
