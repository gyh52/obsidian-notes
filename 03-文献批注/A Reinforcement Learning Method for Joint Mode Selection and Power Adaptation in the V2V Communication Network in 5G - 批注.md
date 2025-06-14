 Mdnotes File Name: [[Zhao_2020_ReinforcementLearning]]

## 总结
1.  <span style="color: rgb(0,0,0)">采用双 DQN（DDQN）方法解决链路在基站模式与自组织模式之间的切换问题</span>
2.  <span style="color: rgb(0,0,0)">优化目标是最大化 V2I 链路的总容量，保证 V2V 链路严格的传输时延和可靠性约束。</span>

## 工作
1.  针对5G通信网络中V2V通信模式选择和功率适配问题，提出了一种基于慢衰落参数和统计信息的强化学习( RL )框架。
2.  以最大化V2I链路总容量为目标，同时保证V2V链路严格的传输时延和可靠性约束。
3.  使用了多智能体双深度Q学习( DDQN )算法。每个V2V链路被视为一个智能体，通过与环境交互，利用更新后的Q网络学习最优策略。
4.  实验验证了算法的收敛性。仿真结果表明，所提方案能够显著优化V2I链路的总容量，保证V2V链路的时延和可靠性需求。