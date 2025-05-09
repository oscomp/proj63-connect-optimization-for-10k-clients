# proj63-connect-optimization-for-10k-clients

### 项目名称 
针对特定场景对connect接口做优化

### 项目描述

- connect()和bind()接口可以指定特定的端口，也可以不指定。不指定的情况下端口将由系统自动分配，分配的范围是/proc/sys/net/ipv4/ip_local_port_range文件配置的端口范围。请将端口范围设置为20000 - 40000。
- 有一个TCP服务端，如果已经连接了9999个客户端，再连接一个客户端，速度很快；如果已经连接了10001个客户端，再连接一个客户端，速度骤然变慢大约十倍。

1. 编写代码复现以上现象，并分析原因
2. 修改connect()接口代码，提升速度，将连接10001个客户端再连接一个客户端场景的连接速度提升至少50%，即达到前者的5倍以上。

### 所属赛道

2025全国大学生操作系统比赛的“OS功能设计”赛道


### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2025全国大学生操作系统比赛”的章程和技术方案要求



### 项目导师

江巍

* gitee jiangwei

* email colordev.jiang@huawei.com

### 难度

中等

### 特征

- 对Linux kernel和编译原理有一定了解
- 熟悉C语言

### 文档

https://gitee.com/src-openeuler/kernel/issues/I2CT3R

https://blog.lucode.net/network-stack/problem-of-performance-degrading-in-linux-src-port-selecting.html

### License

GPLv2 (https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)


## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

### 第一题：在openEuler上复现项目描述中的场景

1. 预期目标是编写代码复现以上现象。

### 第二题：针对该现象，进行内核优化，从而提升该特定场景的connect()接口速度。

2. 预期目标是将connect()接口速度提升至少50%。
