He_2020_DesignAnalysis
Title:: Design and analysis of a short-term sensing-based resource selection scheme for C-V2X networks
Citekey:: He\_2020\_DesignAnalysis
Author:: Xinxin He; Jie Lv; Jiaqi Zhao; Xiaolin Hou; Tao Luo
Date:: 2020-12-11
Journal:: IEEE Internet of Things Journal
Tags:: #非周期 #S-SPS #Mode4 #资源感知
File:: [9098860.html](zotero://open-pdf/0_VYHM7B4T)
Work:: 提出了一种基于短期感知的资源选择（STS-RS）方案。资源单元开始前配置一个短期感知持续时间，在资源选择前进行感知，数据包是否在选定的资源上最终传输取决于感知结果。STS-RS方案旨在减少由于资源选择争用而导致的数据包冲突。
Abstract:: 蜂窝车对万物 (C-V2X) 网络可以通过 Sidelink/PC5 接口支持直接车对车 (V2V) 通信，无需蜂窝基础设施支持。基于感知的半持续调度（SPS）方案允许车辆自主预留和选择无线电资源。然而，分布式SPS算法的共感知特性导致C-V2X分布式通信可能受到资源选择冲突的挑战，特别是在非周期性流量中，导致可靠性较低。在本文中，我们提出了一种基于短期感知的资源选择（STS-RS）方案，以减少由于资源争用而导致的数据包冲突，其中在资源选择之前的资源单元的开头配置短期感知持续时间，而数据包最终是否在所选资源上传输取决于感知结果。此外，还研究了所提出的 STS-RS 方案和 C-V2X 模式 4 中定义的 SPS 方案的性能分析模型。最后，仿真和数值结果表明，与SPS方案相比，STS-RS方案显着减少了数据包冲突并提高了C-V2X直接通信性能。
## 研究背景
在 C-V2X（蜂窝车联网）系统中，非周期性资源是指用于非周期性流量的无线电资源。这些资源的选择通常是随机的，特别是在无覆盖情况下，这可能导致较低的传输可靠性，因为这样的随机资源选择会导致资源争用。
## 研究目的
在 C-V2X 分布式通信中，对于非周期性流量，采用的是在SW（感知窗口）中进行的随机资源选择。例如，如果一辆车需要为非周期性消息传输预留新资源，它可以在SW中随机选择一个候选资源并为传输预留。因此，不同车辆的共同候选资源数量可以近似为SW中的资源数量​。然而，C-V2X模式4中非周期性流量的这种随机资源选择会导致严重的数据包冲突，并降低传输可靠性。
为了减少资源争用带来的数据包冲突，提出了一种基于短期感知的资源选择（STS-RS）方案。
## 研究技术
基于Mode4 S-SPS
资源池设置：一个子帧子信道被划分为多个symbols，红色窗口是短期感知部分。
![\<img alt="" data-attachment-key="RX3RHNAC" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F2UZV3YMS%22%2C%22annotationKey%22%3A%222Y29UPVI%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%2211212%22%2C%22position%22%3A%7B%22pageIndex%22%3A3%2C%22rects%22%3A%5B%5B312.677%2C659.022%2C564.646%2C746.526%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FGDRDIAXT%22%5D%2C%22locator%22%3A%2211212%22%7D%7D" width="420" height="146" src="05-附件/RX3RHNAC.png" ztype="zimage">](RX3RHNAC.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FGDRDIAXT%22%5D%2C%22locator%22%3A%2211212%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/GDRDIAXT">He 等, 2020, p. 11212</a></span>)</span>
感知窗口：选择前进行短期的感知，如果没有确定候选资源，再进行一次短期感知。
![\<img alt="" data-attachment-key="NUTB7HBS" data-annotation="%7B%22attachmentURI%22%3A%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2F2UZV3YMS%22%2C%22annotationKey%22%3A%226RYLVKXF%22%2C%22color%22%3A%22%23ffd400%22%2C%22pageLabel%22%3A%2211212%22%2C%22position%22%3A%7B%22pageIndex%22%3A3%2C%22rects%22%3A%5B%5B319.003%2C430.774%2C556.212%2C523.549%5D%5D%7D%2C%22citationItem%22%3A%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FGDRDIAXT%22%5D%2C%22locator%22%3A%2211212%22%7D%7D" width="395" height="154" src="05-附件/NUTB7HBS.png" ztype="zimage">](NUTB7HBS.png)\
<span class="citation" data-citation="%7B%22citationItems%22%3A%5B%7B%22uris%22%3A%5B%22http%3A%2F%2Fzotero.org%2Fusers%2F10122808%2Fitems%2FGDRDIAXT%22%5D%2C%22locator%22%3A%2211212%22%7D%5D%2C%22properties%22%3A%7B%7D%7D" ztype="zcitation">(<span class="citation-item"><a href="zotero://select/library/items/GDRDIAXT">He 等, 2020, p. 11212</a></span>)</span>
## 研究内容
**基于短期感知的资源选择（STS-RS）**
资源单元开始前配置一个短期感知持续时间，然后在资源选择前进行感知，数据包是否在选定的资源上最终传输取决于感知结果。STS-RS方案旨在减少由于资源选择争用而导致的数据包冲突，这种方案对于周期性和非周期性流量都有效，而且不需要额外的控制信号开销或其他无线电技术的辅助​。
## 实验结果
对比STS-RS方案和3GPP定义的非周期性流量的随机资源选择方案的仿真结果显示，STS-RS方案平均可将中断概率降低15%
<span style="color: rgb(55, 65, 81)">不足：</span>
1.  **<span style="color: var(--tw-prose-bold)">增加的通信延迟</span>**:
    *   <span style="color: rgb(55, 65, 81)">短期感知过程需要额外的时间来评估可用资源，这可能导致通信延迟增加，特别是在对实时性要求较高的应用场景中。</span>
2.  **<span style="color: var(--tw-prose-bold)">资源利用效率可能降低</span>**:
    *   <span style="color: rgb(55, 65, 81)">如果多个车辆同时放弃了相同的资源，可能会导致这些资源未被充分利用。</span>
3.  **<span style="color: var(--tw-prose-bold)">复杂性增加</span>**:
    *   <span style="color: rgb(55, 65, 81)">实施短期感知需要更复杂的算法和硬件支持，可能增加系统的整体复杂性和成本。</span>
4.  **<span style="color: var(--tw-prose-bold)">能源消耗增加</span>**:
    *   <span style="color: rgb(55, 65, 81)">对于依赖电池供电的车辆，进行持续的感知活动可能会导致更高的能源消耗。</span>
5.  **<span style="color: var(--tw-prose-bold)">感知准确性的挑战</span>**:
    *   <span style="color: rgb(55, 65, 81)">在高速变化的通信环境中，短期感知的结果可能不够准确，导致选择的资源并非最优。</span>
6.  **<span style="color: var(--tw-prose-bold)">干扰和冲突管理</span>**:
    *   <span style="color: rgb(55, 65, 81)">在拥挤的网络环境中，即使进行了短期感知，资源冲突和干扰的管理仍然是一个挑战。</span>
7.  **<span style="color: var(--tw-prose-bold)">实时性问题</span>**:
    *   <span style="color: rgb(55, 65, 81)">网络条件快速变化时，短期感知结果可能在实际传输时已不再适用，影响数据传输的实时性和可靠性。</span>
8.  **<span style="color: var(--tw-prose-bold)">动态环境适应性</span>**:
    *   <span style="color: rgb(55, 65, 81)">在高动态的车联网环境中，例如高速公路上，短期感知基于资源选择的策略可能需要频繁调整和更新，以适应环境变化。</span>
## 可借鉴
在 C-V2X 系统中，非周期性流量通常采用随机资源选择机制，尤其是在无覆盖情况下。这种机制会导致较低的传输可靠性，可能导致资源争用加剧。
