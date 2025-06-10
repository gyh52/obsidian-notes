 Mdnotes File Name: [[System-Level Simulation Platform of C-V2X Mode 4 Integrating CarMaker and NS-3]]

# 批注

批注

摘要

考虑到C - V2X模式4对于实际V2X通信场景的重要性，本文基于交通仿真器CarMaker和网络仿真器( NS ) 3搭建了C - V2X模式4的系统级仿真平台。

1. 为了创建逼真的车辆轨迹，在CarMaker中创建典型的车道模型和车辆模型。
2. 在NS3中，对C - V2X Mode 4协议栈的信道模型和服务模型进行了修改和扩展，使其支持车载节点间的C - V2X Mode 4通信。

基于我们的仿真平台进行了性能分析，从数据包接收率( PRR )和平均时延方面考察了不同因素对传输性能的影响。