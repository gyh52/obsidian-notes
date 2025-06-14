 Mdnotes File Name: [[Latif_2022_TDMABasedMAC]]

# 论文结构：

第一部分引言。
第二部分介绍相关工作。
第三节介绍了必要的背景并阐述了问题。
第四节介绍了所提出的协议。
第五部分详细介绍了仿真研究。
第六部分对全文进行了总结。

# 相关工作：

1.  ADHOC-MAC以**TDMA**方式交换周期性消息。
2.  VeMAC通过**定义时隙释放预防条件**，进一步改进了广播机制。VeMAC和MoMAC采用**帧划分技术**，形成固定大小的分区，减少数据包碰撞。
3.  A-VeMAC、AODMAC和SAMD采用**自适应帧划分**，即根据各自路段的车辆密度动态调整划分长度。
4.  Fine-grained MAC使用**动态信标速率**来解决时隙不足问题，但对合并冲突使用与MoMAC相同的解决方案。
5.  PTMAC使用基于**碰撞预测的机制**来减少合并碰撞场景引起的数据包碰撞。使用两辆中间车辆预测了相距三跳的两辆车之间的槽合并碰撞。两个中间车辆通过检查一跳集合可以检测到两个不同车辆使用的共同时隙。中间车辆然后根据易感车辆的速度和方向将这种检测归类为可能的碰撞。然后指示其中一辆车腾空并获取新的时隙。
6.  通过**调整发射功率**来减少因合并碰撞场景导致的数据包碰撞次数，即对于较高的车辆密度，车辆降低发射功率以减少其通信范围，反之亦然
7.  利用相邻车辆的**接收信号强度进行时隙管理**。
8.  每个车辆根据从相邻车辆接收到的信息计算一个系数，称为危险系数。然后，每辆车**根据危险系数的值调整其信标速率**。较大的值意味着更危险的情况，因此车辆增加其信标速率，反之亦然。
9.  基于车辆的**运动预测**来缓解数据包冲突。

# 问题：

1.  接入冲突：
    **两跳邻域**内有多个车辆同时选择相同的空闲时隙进行传输。
2.  合并冲突
    ![[Pasted image 20230221165237.png|600]]
3.  **后续访问冲突**：合并冲突后重新接入又发生接入冲突

这三种冲突情况：以1帧5个时隙为例
![[Pasted image 20230221165307.png|800]]
# 协议
![[Pasted image 20230221165318.png|600]]
已知车辆集合( CVS )
先前已知车辆集合( PVS )

## 基本原理
通过**第三方时隙合并碰撞机制、时隙建议机制和绑定分解机制**缓解数据包冲突。避免数据包碰撞后的**后续访问冲突**。

## 优点
1. 减少了整体的丢包率
2. 避免了两个连续的周期性消息之间的长时间延迟

当车辆之间发生合并碰撞时，

1.  **自时隙合并碰撞**。车辆让出时隙，并请求新时隙。撤离的车辆可以通过**时隙提示机制**从已知的相邻车辆收到选择新时隙的建议。
2.  **第三方时隙合并碰撞**。通过**连接中断机制**，指示其中一辆车在数据包碰撞中保留时隙，其他车辆腾空时隙，避免进一步的数据包碰撞。

### CVS和PVS的定义
CVS：由车辆ID和时隙号组成的有序对。表示直接位于本车通信范围内的已知车辆。
PVS：没有成功接收到数据包的上一帧里CVS中的车辆，则在这一帧中划分到PVS中，构成**可能遇到合并碰撞的车辆**。
![[Pasted image 20230221165331.png|350]]

已知车辆和未知车辆：
在上一帧属于CVS（本车通信范围内）则是已知车辆，不属于CVS（通信范围内）是未知车辆。

## 自时隙合并碰撞检测
在理想信道条件下，令车辆V拥有时隙tv，V在当前时隙tc接收来自源车辆Y的数据包。
- 如果Y为未知车辆，则在CVS（V）中加入Y时隙信息，不检查丢槽情况。
- 如果Y是已知车辆，则检查丢槽情况。
	如果V在CVX（Y）中，说明没冲突，V保留时隙。
	如果不在，说明V发生冲突，V放弃该时隙。

## 第三方时隙合并碰撞检测
除了为自己的时隙检测，还检测在车辆通信范围内发生的任何其他合并碰撞。
![[Pasted image 20230221165345.png|650]]
  
## 时隙推荐机制
![[Pasted image 20230221165405.png|700]]

## 连接中断机制
![[Pasted image 20230221165535.png|800]]

## 数据包结构
![[Pasted image 20230221165422.png|700]]
- 第一个字段Source vehicle ID是数据包发送者的车辆ID。
- FTflag是当车辆通过新选择的时隙发送其第一次传输时设置的。在断链机制中使用。
- 如果一辆车要向另一辆车提出空闲时隙，则使用建议字段。
- 在基于TDMA的MAC协议中，每个车辆发送其一跳邻居的信息，即周期性消息，也叫帧信息( FI )。
- MCCM - MAC在FI中的每个条目需要标志A和B，用来表示CVS等信息。