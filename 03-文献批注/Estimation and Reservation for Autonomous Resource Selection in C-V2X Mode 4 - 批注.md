 Mdnotes File Name: [[Sabeeh_2019_EstimationReservation]]

# 工作
每个车辆列出接收到的数据包中**具有相同随机计数器的所有资源位置**。这使得每个终端可以估计在下一次资源选择中哪些位置是空闲的。当随机计数器达到零时，列表中的下一个位置将被选择。

# 目的
我们提出了一种算法来增强性能，旨在降低碰撞率和提高PRR。其思想是每个车辆列出接收到的数据包中具有相同随机计数器的所有资源位置。这使得每个终端可以估计在下一次资源选择中哪些资源位置将是空闲的。此外，当随机计数器达到零时，列表中公布的下一个位置将是当前位置。这样车辆不需要依赖感知过程，资源利用率得到提高。我们的仿真表明，与S - SPS相比，我们提出的算法的性能有了显著的提高。

<span style="color: #494949">ERRA的工作方式如下：</span>

 <span style="color: #494949">用户设备UEi不断分析数据包，并记录从感知范围内的节点收到的解码SCI。</span>
 <span style="color: #494949">然后UEi在创建的列表A中保留所有具有相同RC值的数据包位置。</span>
 <span style="color: #494949">当RCi达到5时，预估的资源位置被从列表A中选出，然后UEi它为下一个资源位置（UEi, UE3, UE7, UE8）。</span>
 <span style="color: #494949">UEi不断检查预定的下一个位置，以确保它在下一次重选中可用（UE2）&nbsp;</span>
 <span style="color: #494949">当RCi达到零时，UEi选择的下一个资源位置被占用，并产生新的RC（UE1）</span>
    

<span style="color: #494949">对SCI进行小扩展（大约两个字节），记录下一个资源的位置、RC和碰撞位置（如果存在）。不依赖于传感过程。</span>

<span style="color: #494949">本文中RCi值在6到15之间，但新的RCi应该与同一子帧中广播的其他RC值兼容（UE10、UE11、UE12、UE13。）&nbsp;</span>

<span style="color: #494949">通过这种方式，为下一个重新选择的位置保留相同的资源位置。UEi资源的下一个位置或当前位置的可用性可能会发生变化，当一个新的UE进入邻域，其资源位置被宣布为UEi的下一个位置，如果与当前资源位置导致数据包碰撞（UE4），它可以通过SCI数据向所有其他UE表明碰撞的资源位置。</span>

协议
![[Pasted image 20230301135905.png]]
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FE2MVVKTF%22%5D%2C%22locator%22%3A%223%22%7D%5D%2C%22properties%22%3A%7B%7D%7D">(<span class="citation-item">Sabeeh 等, 2019, p. 3</span>)</span>

结论：

令人印象深刻的结果是，所提出的算法的碰撞比远远低于S - SPS算法的碰撞比几乎为零并且保持稳定。

对于不同的车流密度，数据包碰撞也是稳定的。