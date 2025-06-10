 Mdnotes File Name: [[Jeon_2020_ExplicitReservationAugmented]]

# 批注
在本文中，我们提出了一种针对C - V2X侧链路模式4的预留机制，该机制补充了标准SPS，在面对拥塞和通信范围边缘的情况下显著提高了性能。特别地，我们证明了如果预留资源比实际使用预留资源至少提前1秒，预留将获得最好的性能。

基本安全消息( BSMs )
BSM之间的间隔被称为资源预留间隔( Resource Retention Interval，RRI )

问题：
1.  SPS资源重选虽然是随机选择，即使是不在同一子帧的车辆仍有比较高的碰撞概率。
2.  半双工限制导致在同一子帧的车辆无法被感知，可能会选择同一资源，发生碰撞。

![[Pasted image 20230302161835.png|500]]
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FEACMPLPP%22%5D%2C%22locator%22%3A%22147245%22%7D%5D%2C%22properties%22%3A%7B%7D%7D">(<span class="citation-item">Jeon 和 Kim, 2020, p. 147245</span>)</span>

协议：

我们的建议的主要目标是通过一个额外的保留机制来增强SPS，该机制具有三个与SPS相反的特性。

1.  Explicit：每辆车明确告知其他车辆重新选择的资源位置
2.  Early：提前预留位置
3.  Repeated：由于提前预留，导致重复发送信息，提高了接收率

![[Pasted image 20230302161854.png|550]]
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FEACMPLPP%22%5D%2C%22locator%22%3A%22147248%22%7D%5D%2C%22properties%22%3A%7B%7D%7D">(<span class="citation-item">Jeon 和 Kim, 2020, p. 147248</span>)</span>

在一开始，车辆选择使用传统SPS的启动资源位置和第一个数据包运行的RC值，同时选择下一次运行的启动资源位置并公布。

对于性能指标，我们使用包接收率( PRR )和包接收间隔时间( PIR )。它们在3GPP TS 36.885中的定义如下：

数据包接收间隔( Packet Inter-Reception，PIR )：PIR是车辆V向W发送的两个不同数据包连续成功接收之间的时间间隔。

包接收率( Packet Reception Ratio，PRR )：对于每个发送的数据包，PRR由X / Y计算，其中Y为距离发射端( a , b)范围内的车辆数，X为Y中成功接收的车辆数。

优势：

这项工作的未来扩展可能是在公平领域，特别是明确的保留可以被推翻或妥协的条件，以防止可能的先发制人的资源占用。