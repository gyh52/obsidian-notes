Wu\_2019\_MBRMapbased
Title:: MBR: A map-based relaying algorithm for reliable data transmission through intersection in VANETs
Citekey:: Wu\_2019\_MBRMapbased
Author:: Jingbang Wu; Huimei Lu; Yong Xiang; Rui Wu; Feng Wang
Date:: 2019-10
Journal:: IEEE Transactions on Intelligent Transportation Systems
Tags:: #Geohash , #交叉路口 , #信道协作 #地理位置 
File:: [8527669.html](zotero://open-pdf/0_N33TWWAQ)
Work:: 使用 Geohash 编码进行中继区域表示，并根据实时交通状况动态选择中继节点
Abstract:: 近年来，针对城市车载 ad-hoc 网络（VANET）提出了许多路由协议。然而，这些协议的一个共同问题是没有仔细考虑交叉路口的建筑物阴影效应。因此，这些路由协议的性能可能会下降，因为交叉路口的数据传输会受到建筑物阴影的严重影响。为解决这一问题，本文在 MAC 层提出了基于地图的中继算法 MBR，以提高城市 VANET 中路由协议的性能。为了提高交叉路口数据传输的可靠性，MBR 在 MAC 层创新性地利用了数字地图和 Geohash 编码系统来中继数据包（帧），并根据节点与交叉路口的相对位置选择最佳中继节点。本文提出了两个版本的算法：MBR-S 利用单个 IEEE 802.11p 无线电；而 MBR 则利用 IEEE 802.11p 信道和 Sub-1GHz 信道的协作，后者在交叉路口的通信范围比 MBR-S 更大。我们的实际实验和大量仿真都证明，MBR-S 能显著提高最先进的 VANET 路由协议的性能，而两个信道的协作还能进一步提高性能。
## 研究目的
研究关于城市交叉路口更可靠的数据传输方法。
## 研究技术
MBR 算法：使用数字地图和 Geohash 编码系统进行数据包中继，根据节点和路口位置优化中继节点选择。
## 算法内容
MBR算法：
1.  **中继区域的 Geohash 编码**：MBR 算法使用 24 位 Geohash 编码长度来准确表示交叉口的中继区域。中继区由交叉口的中心网格及其邻近网格组成，可准确定位交叉口及其周围区域。
2.  **地图-Geohash 映射和中继区计算**：通过地图-Geohash 映射获得交叉口的 Geohash 代码，然后计算中继区的 Geohash 代码集。中继区计算算法在 MBR 中按数据包级别运行，并使用广度优先搜索（BFS）来遍历路段。
3.  **广播节点位置**：每个节点以 Geohash 形式广播其当前位置。通过比较这些 Geohash 代码，可以计算出节点和中继区域的相对位置。这样，系统就能动态确定数据包是否需要中继，如果需要，就能在中继区域内选择最佳中继节点。
4.  **选择中继节点**：该算法从邻居中选择一个中继节点，确保它位于信源和接收器之间交叉点的中心区域。这种选择可确保所选节点位于源节点的完美接收区域，而目的节点位于所选节点的完美接收区域。
## 实验结果
通过实际实验和仿真证明，MBR 算法显著提高了 VANET 路由协议的性能，尤其是在协同使用 IEEE 802.11p 和 Sub-1GHz 信道时。
## 可借鉴
创新性地使用 Geohash 编码进行中继区域表示，并根据实时交通状况动态选择中继节点，可应用于其他需要在复杂城市环境中进行高效、可靠数据传输的场合。
每个节点以 Geohash 形式广播其当前位置。通过比较这些 Geohash 代码，可以计算出节点和中继区域的相对位置。
