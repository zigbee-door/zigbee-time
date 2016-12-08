﻿


# zigbee-time

## 总体进度安排

| 时间                 | 任务                                   | 完成度 |
| :-------------       |:-------------                          |:-----  |
| 2016/11-2016-12      | zibee路由协议的论文查看和算法成果研究  | 作废    |
| -                    | 门锁程序和基站程序的设计(前期先进行实验数据的获取,不实现应用部分)   |   5%  |
| -                    | express和tcp编写                    |    20%  |
| 2016/12-2017/01      | 设计zigbee路由算法  | 作废    |
| -                    | 实现门锁离线程序,基站和pc通信程序   |   0%  |
| -                    | 实现总通信协议                      |    0%  |
| 2016/01-2017/03      | 实现总体设计  | 0%     |
| -                    | 编写论文  |   30%  |

## 日进度

| 时间          | 类型           | 进度    |
|:------------- |:-------------  |:-----   |
| 2016/10/31    | zigbee-http    | socket.io成功 |
| 2016/11/01    | zigbee-http    | 添加mongodb配置 |
| 2016/11/02    | zigbee-http    | 添加redis配置 |
| 2016/11/03    | zigbee-http    | 添加登录功能 |
| 2016/11/04    | zigbee-tcp     | 添加进程和错误日志,开启多进程,添加守护进程,添加tcp服务 |
| 2016/11/05    | zigbee-tcp     | 添加tcp服务日志,模拟socket连接成功 |
| 2016/11/06    | zigbee-tcp     | socket连接状态通过redis发布成功 |
|               | zigbee-http    | 成功订阅tcp服务的socket连接状态  |
| 2016/11/07    | zigbee-http    | redis订阅数据成功通过socket.io发送至浏览器 |
|               | zigbee-tcp     | 增加基站数据字段,至此,tcp -> redis -> http -> browser路线走通  |
| 2016/11/08    | zigbee-http    | 添加图表曲线插件,引入angular |
|               | zigbee-tcp     | 连接真实设备两台成功  |
| 2016/11/09    | zigbee-http    | zigbee路由协议研究,决定使用RSSI作为路由算法的主参数 |
| 2016/11/10    | zigbee-lock    | IAR环境的配置,zigbee嗅探器工具的使用 |
| 2016/11/11    | zigbee-lock    | sysclk,led,pcf8563等驱动层和外设层的程序编写和测试,使用PM2休眠一秒钟并唤醒,增加射频模块 |
| 2016/11/17    | zigbee-lock    | ad检测和定时器模块和测试，他人论文的查看，研究了Leach路由算法，但是并不是zigbee协议的路由，重新考虑论文的侧重点 |   
| 2016/11/22    | zigbee-lock    | zigbee方面的论文查看，zigbee协议栈的研究，论文侧重点定论为z-stack协议栈的研究以及RFID读卡器的研究，低功耗仍然作为侧重点，加入zigbee安全机制说明，z-stack协议栈的研究，准备从门锁开始传输电池电量数据构建一整套回路，准备开始写论文框架 |   
| 2016/11/23    | 论文    	 | 编写论文，写出第一章绪论第一小节研究背景和意义。研究了z-stack协议栈通信的点播，组播和广播，仍然有很多不清楚的地方需要深入研究。 |  
| 2016/11/24    | 论文   	 | 编写论文，写出第一章绪论第二小节国内外研究现状，参考了大量的国外文献。|  
| 2016/11/25    | 论文   	 | 编写论文，写出第二章绪论第一二三小节，参考了大量的国外文献。|  
| 2016/11/28    | 论文    	 | 编写论文，写出第三章一二小节。测试了系统移动式设备如手机的访问可行性。|  
| 2016/11/29    | 论文    	 | 编写论文，写出第三章三小节第一小点。|  
| 2016/12/01    | 论文    	 | 编写论文，写出第三章三小节第二三小点以及第四小节，调整章节顺序。|  
| 2016/12/02    | 论文    	 | 编写论文，调整第二章的章节，新增2.4小节，编写2.4小节的一二两小点。|  
| 2016/12/03    | 论文    	 | 编写论文，编写2.4小节第三小节。|  
| 2016/12/05    | 论文    	 | 编写论文，编写2.4小节第4,5小节，新增安全服务第6小节，感觉论文写的有点糅杂，顺便参考论文的质量也参差不齐，论文的口语化偏重，仍然需要大量的查阅别人的论文，之后需要标记写的好的章节以及需要重新修改较多的章节。之前的论文框架写完第二次修改重新审阅。|  
| 2016/12/06    | 论文    	 | 第二章和第三章写完，重新安排时间规划，白天编写门锁和基站以及上位机的通信程序，晚上撰写论文。| 
| 2016/12/07    | zigbee-tcp/http| windows环境运行修复，准备使用z-stack上传数据，建立tcp服务器和客户端的通信机制。| 
| 2016/12/08    | zigbee-base/lock| Z-Stack协议栈的深入研究，包括函数的作用和数据的传输。| 




## 论文目录进度

```javascript

.
├── 基于Zigbee的无线门锁系统设计与实现 
├── 第一章 绪论	
│   ├── 1.1 研究背景与意义   
│   ├── 1.2 国内外研究现状
│   │   ├── 1.2.1 公租房国内外发展状况
│   │   ├── 1.2.2 智能锁国内外发展现状
│   │   └── 1.2.3 Zigbee无线网络研究现状   
│   ├── 1.3 本文的主要工作(未完成)
│   └── 1.4 本文的组织机构(未完成)		
├── 第二章 短距离无线网络中的Zigbee无线网络
│   ├── 2.1 短距离无线网络的分类
│   ├── 2.2 几种短距离无线通信技术的特点比较
│   ├── 2.3 Zigbee无线网络简介
│   │   ├── 2.3.1 Zigbee无线网络组成
│   │   ├── 2.3.2 Zigbee无线网络特点
│   │   └── 2.3.3  Zigbee无线网络的设备类型和拓扑结构
│   ├── 2.4 Zigbee无线网络协议栈
│   │   ├── 2.4.1 Zigbee无线网络的协议层和数据帧
│   │   ├── 2.4.2 物理层(MAC)
│   │   ├── 2.4.3 介质访问控制层(PHY)
│   │   ├── 2.4.4 网络层(NWK)
│   │   ├── 2.4.5 应用层(APL)
│   │   └── 2.4.6 安全服务
│   └── 2.5 本章小节
├── 第三章 系统总体设计
│   ├── 3.1 需求分析
│   │   ├── 3.1.1 无线门锁需求分析
│   │   └── 3.1.2 管理系统需求分析
│   ├── 3.2 系统整体框架
│   ├── 3.3 系统硬件总体设计
│   │   ├── 3.3.1 系统硬件拓扑设计
│   │   ├── 3.3.2 门锁硬件结构
│   │   └── 2.3.3 基站硬件结构
│   ├── 3.3 系统软件层级设计
│   └── 3.4 本章小节
├── 第四章 门锁和基站设计(未完成)
├── 第五章 门锁通讯和管理软件设计(未完成)
├── 第六章 系统实现和测试(未完成)
├── 第七章 总结与展望(未完成)
├── 参考文献(未完成)
├── 附录(未完成)
├── 致献(未完成)
└── 攻读学位期间参加的科研项目和成果(未完成)

```
