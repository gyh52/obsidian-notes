 Mdnotes File Name: [[Lyu_2018_MoMACMobilityAware]]

# 协议

1.  时隙分组：根据底层道路拓扑和道路上的车道分布，考虑车辆的移动性，为每辆车分配一个时隙。
2.  更新两跳邻居信息检测时隙冲突。

# MoMAC 中的时隙分配

1) 当车辆在多车道路段上行驶时，根据车道信息划分时隙集；

2) 当车辆位于交叉路口时，根据交叉路口的拓扑结构划分时隙集；

3) 当车辆进入或离开交叉路口时，根据地理联系将前两种方案拼接在一起。

# 系统模型

1.  采用DSRC无线通信，在本文中讨论如何为 CCH 设计高效可靠的 MAC 协议。
2.  采用了道路的基本拓扑结构和车道分布。由于道路拓扑和车道分布是恒定的，只需知道自己属于哪条道路和哪条车道，这属于分类问题，而不是绝对定位问题，因此GPS 定位不准确和 GPS 暂时短缺对方案的性能影响很小。