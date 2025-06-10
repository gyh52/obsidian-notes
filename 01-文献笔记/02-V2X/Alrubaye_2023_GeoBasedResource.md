Title:: Geo-Based Resource Allocation for Joint Clustered V2I and V2V Communications in Cellular Networks
Citekey:: Alrubaye\_2023\_GeoBasedResource
Author:: Jaafar Sadiq Alrubaye; Behrouz Shahgholi Ghahfarokhi
Date:: 2023-07-31
Journal:: IEEE Access
Tags:: #地理位置 #路由感知 #聚类算法
Work:: 本文通过提出一种路由感知的资源分配方法，结合基于集群的路由和基于地理位置的资源分配，来解决车辆通信系统中的资源分配问题。提出了两种启发式算法，使CHs能够在不显著影响V2V连接的QoS要求的情况下，将一些已分配给V2V通信的RB用于其V2I链接。
File:: [Alrubaye\_Ghahfarokhi\_2023\_Geo-Based Resource Allocation for Joint Clustered V2I and V2V Communications in.pdf](zotero://open-pdf/0_CL4PH737)
## <span style="color: #E65100"><span style="background-color: #f7e5da">📄 研究背景</span></span>
***
随着流动性和车辆数量的不断增加，车辆通信的资源分配效率变得更加困难。为了解决这一问题，人们提出了不同的资源分配方案，但路由感知资源分配在文献中还未得到足够的重视。
## <span style="color: #fcca03"><span style="background-color: #fff8e1">🔎 研究方法</span></span>
***
本文通过提出一种路由感知的资源分配方法，结合基于集群的路由和基于地理位置的资源分配，来解决车辆通信系统中的资源分配问题。
![\<img alt="" data-attachment-key="GMSX4ZQG" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FCL4PH737%22%2C%22annotationKey%22%3A%223ZGIWJCL%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%2282605%22%2C%22position%22%3A%7B%22pageIndex%22%3A4%2C%22rects%22%3A%5B%5B38.554%2C447.861%2C538.13%2C687.904%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FN7NW8SW6%22%5D%2C%22locator%22%3A%2282605%22%7D%7D" width="833" height="400" src="attachments/GMSX4ZQG.png" ztype="zimage">](GMSX4ZQG.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FN7NW8SW6%22%5D%2C%22locator%22%3A%2282605%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/N7NW8SW6">Alrubaye 和 Ghahfarokhi, 2023, p. 82605</a></span>)</span>
1.  DSRC 用于集群内通信，将集群内的车辆连接到 CH。然后，CH 使用蜂窝资源向 BS 发送其 CM 的数据包。未集群的 V2I 车辆通过蜂窝资源直接连接到 BS，并被假定为无 CM 的 CH。CH 与信号强度最高的 BS 关联。
2.  对于 V2V 通信，采用了基于地理位置的资源分配，将区域划分为若干个 SA（带白色数字的黑圈），以便每个 SA 中的车辆都能使用分配给该区域的蜂窝无线电资源。RV2V 资源块被分为 n 个子资源池（SR），对应分好的区域，资源池能重复使用。
3.  按照距离指标和密度指标这两个指标的加权组合，对SA进行聚类。密度指标表示的是这些集群 SA 内部车辆数量的相似程度。
## <span style="color: #2E7D32"><span style="background-color: #f1f8e9">🔬 研究内容</span></span>
***
提出了一种路由感知无线电资源管理算法，该算法可根据路由过程中构建的集群需求管理 V2V 通信资源。
第一种算法在保证 V2V 通信质量的前提下，采用子资源池的方式将未使用的 V2V 资源借给 CH。
第二种算法能够从 V2V 子资源池中借出未使用的 RB。
## <span style="color: #4A148C"><span style="background-color: #f5f5f5">🚩 研究结果</span></span>
***
仿真结果表明，该方法平均提高了约75%的频谱效率，同时保持了V2V通信的质量。
第二种拟议算法比第一种算法显示出更高的频谱效率，但代价是违反了基于地理的 V2V 资源分配方案中基于 SR 的资源分配规则。未来的工作将包括把建议的方法扩展到多蜂窝场景，并在其他 VANET 场景的 RA 中考虑路由感知。<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FN7NW8SW6%22%5D%2C%22locator%22%3A%2282611%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/N7NW8SW6">Alrubaye 和 Ghahfarokhi, 2023, p. 82611</a></span>)</span>
## <span style="color: #006064"><span style="background-color: #e0f7fa">📌 创新点</span></span>
***
本文提出了两种启发式算法，使CHs能够在不显著影响V2V连接的QoS要求的情况下，将一些已分配给V2V通信的RB用于其V2I链接。
## <span style="color: #1565C0"><span style="background-color: #e1f5fe">🔧 借鉴</span></span>
***
