# zigbee-time

## 总体进度安排

| 时间                 | 任务                                   | 完成度 |
| :-------------       |:-------------                          |:-----  |
| 2016/11-2016-12      | zibee路由协议的论文查看和算法成果研究  | 0%     |
| -                    | 门锁程序和基站程序的设计(前期先进行实验数据的获取,不实现应用部分)   |   0%  |
| -                    | express和tcp编写                    |    20%  |
| 2016/12-2017/01      | 设计zigbee路由算法  | 0%     |
| -                    | 实现门锁离线程序,基站和pc通信程序   |   0%  |
| -                    | 实现总通信协议                      |    0%  |
| 2016/01-2017/03      | 实现总体设计  | 0%     |
| -                    | 编写论文  |   0%  |

## 日进度

- 2016/10/31
    - zigbee-http socket.io成功
- 2016/11/01
    - zigbee-http 添加mongodb配置
- 2016/11/02
    - zigbee-http 添加redis配置
- 2016/11/03
    - zigbee-http 添加登录功能
- 2016/11/04
    - zigbee-tcp  添加进程和错误日志,开启多进程,添加守护进程,添加tcp服务
- 2016/11/05
    - zigbee-tcp  添加tcp服务日志,模拟socket连接成功
- 2016/11/06
    - zigbee-tcp  socket连接状态通过redis发布成功
    - zigbee-http 成功订阅tcp服务的socket连接状态
