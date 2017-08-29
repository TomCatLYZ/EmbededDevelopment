# Coprocessor - 协处理器

硬件厂商可以在SOC中添加其它的处理器来协助ARM核心处理器工作。
这样的关系就好像 x86 架构的计算机中，CPU 和显卡的关系一样。
ARM 处理器最多可以和16个协处理器共同工作，从cp0到cp15.

在基于ARM处理器的计算机中，外设(外部设备，次要设备 - peripheral)关联到处理器的方法
通常是
1. 通过将其物理地址映射到 连接ARM 芯片的内存空间中去。
2. 映射到协处理器空间去，再由协处理器连接ARM处理器。
3. 连接到总线上去，再由总线连接ARM处理器。