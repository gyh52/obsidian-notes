 Mdnotes File Name: [[LTE-V2X车联网技术、标准与应用]]

# 车联网

**车联网**

车联网(IoV)

车载自组织网络(Vehicular Ad hoc Networks, VANETs)

车载网络(Vehicular Network, VN)

移动自组织网络(Mobile Ad hoc Networks, MANETs)

专用短程通信(Dedicated Short Range Communication, DSRC)技术

通过蜂窝网络实现的车辆到一切(C-V2X)

## 车联网架构

车载自组织网络是起源于移动自组织网络(Mobile Ad hoc Networks, MANETs)，主要目的是研究车辆的移动性管理、广播和路由协议等通信领域的范畴。

车联网被认为是物联网(Internet of Things, IoT)的一种独特应用。

车联网是物联网与车载自组织网络的结合应用，是智慧交通系统(ITS)提出以后，将通信领域、车辆传感、边缘计算或云计算等技术相结合提出的新概念，适用的范围更广，能够提供的服务也更加全面。

车载网络(VN)则从属于车联网(IoV)三层体系中的网络层。

车联网的网络层有两种标准，一种是发展成熟的专用短程通信(Dedicated Short Range Communication, DSRC)技术，由美国和日本提出和执行，以802.11p为通信协议生成网络。另一种是通过蜂窝网络实现的车辆到一切(C-V2X)，这一标准最多是由中国和欧洲提出的，利用成熟和广泛分布的蜂窝网络来满足车辆环境的低延迟和高可靠性。从技术角度上看，C-V2X的通信可靠性和稳定性均优于DSRC系统；但从商业应用上看，目前DSRC的产业链相对更成熟。在实际应用中，有线网络、广域网和5G蜂窝网络等通信方式也被应用到网络层中。[1]

### 国内外研究情况

2001年，我国《“十五”综合交通体系发展规则》首次提出“智能交通”的概念，并加入政府规划[12]；

2008年，国家自然科学基金委员会为智能交通的发展设立了专门的助研资金，资助高校科研团队展开相关课题研究，为之后我国车联网的快速发展奠定了理论基础；

2010年，国家863计划首次提出并公开了两个车联网相关项目，旨在缓解我国交通车辆密度大的问题；十二五期间，工信部发布《物联网产业“十二五”规划》，对车联网的市场价值进行了肯定，提出优先发展车联网的战略计划[13]；

2015年，我国工业部出台车联网往后5年的发展计划书：《车联网发展创新行动计划》，对车联网标准化体系的形成提出了新的要求；

2018年，我国在国际智能产业博览会上发布《中国车联网产业发展研究》白皮书，提出我国车联网结合5G技术，研究发展已经进入全新的阶段。

自从2016年开始，我国互联网巨头百度、阿里、腾讯、华为等公司纷纷开始投入资金加入车联网的研究大军，并取得了较多的成果。

在2018年世界移动通信大会上，华为发布了国际首款支持LTE-V通信的芯片——Balong 765，从底层技术出发，为5G车联网的通信提供了新的技术；

在2018百度人工智能开发大会上，百度发布了小度车载OS，基于语音识别技术以及视觉感知技术，小度车载OS可以在车联网环境中为车主提供智能且个性化的服务；

在2018年云栖大会上，阿里发布了AliOS 2.0汽车操作系统，重新定义了“互联网汽车”的相关标准，提供更好的驾车体验。

目前，我国三大电信运营商（移动、电信、联通），华为、中兴等电信基础设施提供商，以及互联网巨头阿里、腾讯等都已经加入全球化组织5G汽车联盟（5G Automotive Association，5GAA）[2]

## 通信技术

专用短程通信（dedicated short range communica-tion，**DSRC**）技术

基于蜂窝移动通信系统的**C-V2X**（cellular vehicle to everything）技术（包括**LTE-V2X和5G NR-V2X**）。

3GPP（The 3rd Generation Partnership Project）

基于LTE系统的LTE-V技术

### 国内外研究情况

美国的V2X通信研究主要围绕DSRC展开。在美国交通部与密歇根大学的支持下，通过SafetyPilot[4]、MCity[5]等项目验证了DSRC的有效性，并测试智能网联汽车技术。

美国于2016年12月颁布了关于联邦机动车安全标准中V2V通信的NPRM（notices of proposed rule making），对V2V通信设备的工作频段、通信能力、市场渗透等给出了建议。

2017年6月，SAE（Society of Automotive Engineers）筹备成立了C-V2X工作组[6]，开展增强应用、直通通信等研究。

欧洲各国开展了Drive C2X[7]、C-ITS corridor[8]、simT D[9]等项目，对道路安全、交通管理与环境保护等应用进行了测试验证。

日本于2012年2月发布了700 MHz频段的10 MHz用于车车/车路防碰撞安全应用的规范ARIB STD-T109[10]；分别在广岛和东京进行了外场测试，并已开始规模测试。

2010年大唐电信科技产业集团率先开始面向智能交通应用的LTE车联网技术研究，笔者在2013年代表大唐首次公开提出基于LTE系统的LTE-V技术[11,12]，现已成为3GPP（The 3rd Generation Partnership Project）的LTE-V2X标准。

## LTE-V2X

LTE-V2X作为面向车路协同的通信综合解决方案，能够在高速移动环境中提供低时延、高可靠、高速率、安全的通信能力，满足车联网多种应用的需求，并且基于TD-LTE通信技术，从而能够最大程度利用TD-LTE已部署网络及终端芯片平台等资源，节省网络投资，降低芯片成本。[3]

## C-V2X

早期阶段通过LTE-V2X技术可以提高交通效率，加速智慧交通的建设，支持辅助驾驶；中远期阶段通过5G NR-V2X技术，同时结合大数据、云计算、人工智能、高精度定位等新兴技术，将实现更短的时延以及更高的可靠性，进一步推进无人驾驶技术的演进。[2]

### C-V2X术语表

数据资源(Transport Block，**TB**)：

资源块(Resource Blocks, **RBs**)

侧链路控制信息(Sidelink Control Information，**SCI**)

物理侧链控制信道(Physical Sidelink Control Channel，**PSCCH**)

物理侧边链路共享信道(Physical Sidelink Share Channel，**PSSCH**)

混合自动重传请求(Hybrid Automatic Repeat reQuest，**HARQ**)

用户设备(User Equipment，**UE**)

无线接入网(Evolved Universal Terrestrial Radio Access Network，**E-UTRAN**)

数据包投递率(Packet Delivery Ratio，**PDR**)

数据包接收率(Packet Reception Ratio，**PRR**):对于每个发送的数据包，PRR由X / Y计算，其中Y为距离发射端( a , b)范围内的车辆数，X为Y中成功接收的车辆数。

延迟(**Delay**)

误块率(Block Level Error Rate，**BLER**)

半静态调度(Semi-Persistent Scheduling，**SPS**)

调度请求(Service Request，**SR**)

候选资源”(Candidate Resources，**CR**)

候选单子帧资源(Candidate Single-subframe Resources，**CSRs**)

平均参考信号接收功率(Reference Signal Received Power，**RSRP**)

信号强度指示(Received Signal Strength Indication，**RSSI**)

资源预定间隔(Resource Reservation Interval，**RRI**)

资源重选计数器(Resource Reservation Counter，**RC Counter**)

信道繁忙率 （Channel Busy Ratio, **CBR**）

数据包接收间隔( Packet Inter-Reception，**PIR** ): 车辆V向W发送的两个不同数据包连续成功接收之间的时间间隔。

#### **LTE-V2X资源池**

**Mode 3**

其中SPS在传统LTE-V2X上增强，支持夸载波调度

UE向基站发送请求，基站根据UE情况进行调度

**Mode 4**

感知+SPS相结合

**已有优化**

1.     标准算法不变调整参数。

a)       分析可变参数对资源分配影响

b)      资源预定间隔对数据包投递率有显著影响

c)       车辆密集时，SPS中重新选择资源的过程，影响小，因为资源少，很可能再次选择同样的资源。

2.     对3GPP标准的Sensing+SPS算法进行修改或扩展

a)       较大数据包不预定直接传输，较小的数据包预定资源

b)      更早执行资源重选过程，提前通知其他车辆

c)       强制更改RC值解决预期冲突

d)      分离控制信息与数据包，携带预定信息[4]

参考文献

[1]邓雨康,张磊,李晶. 车联网隐私保护研究综述_邓雨康[J]. 计算机应用研究: 1-18.

[2]张敏. 基于5G的车联网组网技术研究_张敏[D]. 南京邮电大学, 2020.

[3]陈山枝,胡金玲,时岩,等. LTE-V2X车联网技术、标准与应用_陈山枝[J]. 电信科学, 2018, 34(4): 1-11.

[4]王巨震,江昊,陈琪美,等. C-V2X资源分配方法研究综述[J]. 太赫兹科学与电子信息学报, 2022, 20(1): 1-7.