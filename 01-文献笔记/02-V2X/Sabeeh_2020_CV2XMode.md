# 信息
Author:: Saif Sabeeh, Krzysztof Wesołowski
Date:: 2020-08
Journal:: 2020 IEEE 31st Annual International Symposium on Personal, Indoor and Mobile Radio Communications
Citekey:: Sabeeh_2020_CV2XMode
Tags:: #C-V2X #S-SPS #Mode4 #优化信道冲突 #增加冗余 
Work:: 基于S-SPS，本文引入的ERRA扩展( E-ERRA )解决预分配资源的车辆在重选过程前，刚离开或出现在广播范围内时，预留资源丢失的问题。在ERRA的基础上，创建备份的资源位置列表。
DOI:: [10.1109/PIMRC48278.2020.9217297](https://doi.org/10.1109/PIMRC48278.2020.9217297)
PDF:: [Sabeeh 和 Wesołowski - 2020 - C-V2X Mode 4 Resource Allocation in High Mobility .pdf](zotero://open-pdf/library/items/HL5DHV8V)
Local Library:: [Local library](zotero://select/items/1_GI33P47R)

# 工作
在ERRA的基础上，创建备份的资源位置列表
# 协议
- 原SPS候选资源列表为ListA，把剩余的资源（依旧满足同一RC值）列为ListB作为备份列表。
- 如果下一个资源位置的可用性因任何原因而降低，则将预留的资源位置替换为ListB中S - RSSI最低的资源位置，并再次公布，作为下一次重选资源分配。
- 这样就避免了进入感知区域的新车使用资源的冲突，以及一辆预留资源的车辆被检查出感知范围。
- 当RC达到零时，将使用下一个资源位置，并生成新的RC内容。新的RC范围应排除同一子帧中所有接收数据包的RC值，以避免进一步的资源分配冲突。
# 结论
与S-SPS相比，所提E-ERRA算法的PRR、D-CR和平均CR均有显著提高。E - ERRA算法在不同车辆密度下的平均CR表现出良好的稳定性和可靠性。

# 批注
![[C-V2X Mode 4 Resource Allocation in High Mobility Vehicle Communication - 批注]]