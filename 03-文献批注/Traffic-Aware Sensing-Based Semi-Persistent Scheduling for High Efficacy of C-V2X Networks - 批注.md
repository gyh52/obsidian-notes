 Mdnotes File Name: [[Chourasia_2021_TrafficAwareSensingBased]]

# 批注
本文详细阐述了pKeep和RC对C - V2X系统整体性能的影响。然后提出了一种新的算法，称为交通感知SPS ( TA-SPS )，该算法通过车辆广播的周期性协作感知消息( CAMs )估计道路交通的当前密度来优化配置这些参数。通过减少资源碰撞次数，TA - SPS提高了C - V2X系统的传输可靠性。通过大量的仿真研究，我们展示了在混合道路交通场景中，TA - SPS如何优于传统SPS。

p Keep (保留无线电资源的概率)

Bazzi等人发现通过调节SPS中的pKeep，可以控制系统的PDR和UD。得出pKeep足以控制系统性能，无需修改RC的结论。

MAC层参数pKeep和RC决定了重复使用之前选择的无线资源的最大持续时间，而不需要重新运行SPS算法供车辆选择无线资源。

首先，车辆从RC范围中选择一个随机值，称为RCx，并使用相同的选定资源进行RCx连续传输。每次车辆发送一个数据包，RCx的值都是递减的。
当RCx为0，则使用pKeep决定是否为其后续传输重用相同的资源。

协议：
1. 从接收到的CAM消息中统计发送方的总数（统计邻居总数）
2. 估计当前流量密度( D ) 
	
IF ( D < 0.12veh / m)
	LOW
ELSE IF ( D < 0.24veh / m)
			MEDIUM
		ELSE 
			HIGH
			
3. 将p Keep和RC调整为基于当前交通情景的实证研究中得到的最优设置
![[Pasted image 20230528213459.png|700]]