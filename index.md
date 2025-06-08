---
layout: cv
title: 王国毓
email:
  url: mailto:wangguoyu7777@me.com
  text: wangguoyu7777@me.com
phone: 13274475156
homepage:
  url: https://guoyu.wang
  text: guoyu.wang
# photo: /assets/img/photo.jpg
---

# 王国毓

<!--
include contact information from the front matter
Supported arguments:
    - homepage: url, text
    - phone
    - email
-->

{% include cv-photo.html %}

{% include cv-contact.html %}

## 教育经历

### **吉林大学** `2019.9 - `

```
吉林长春
```

- 计算机系统结构 博士（在读）
- 指导教师：车喜龙 & 胡俊成


### **吉林大学** `2015.9 - 2019.6`

```
吉林长春
```

- 软件工程 学士


## 研究内容

### **将 NVM 高效、优雅、透明地集成到现有存储堆栈** 
_技能点：内核开发、C语言、NVM优化、文件系统设计、一致性算法、模型检查、TLA+_

- 观察：磁盘文件系统由于有 DRAM 缓存的加持，在大部分缓存命中的读或异步写情况下性能较优（这也是许多应用程序的主要访存特征）。NVM 文件系统往往利用 NVM 介质服务全部读写请求。由于 NVM 性能往往弱于 DRAM，这使得其优势相比传统磁盘文件系统具有局限性（仅体现在有大量同步写入的工作负载上）。
- 本工作提出 NVLog，拟在*保留 DRAM cache* 性能优势的基础上*利用 NVM* 的高速持久化特性，通过*选择性吸收同步写入*来精准绕过缓慢的磁盘 IO 路径。NVLog 被设计为在 VFS 层内部拦截并记录同步调用的 WAL，保持了对上层应用和底层 FS 的透明。相比其他工作，NVLog 可以提供更高的运行效率（精准吸收&无索引）和更低的 NVM 空间占用（日志可回收）。
- 考虑到 DRAM、NVM、磁盘混合异构存储系统中可能存在时序、粒度和并行三方面**崩溃一致性挑战**，本工作进一步基于形式化的崩溃一致性定义给出这些问题的解决方案，并使用*形式化验证（模型检查）*方法证明所提出方案的正确性。
- 本工作部分成果已发表在 **FAST '25**，为吉林大学在系统和存储领域首篇顶会文章。


## 专业经历

### **阿里云** `2025.5 - `
```
面向高吞吐场景的下一代互联网存储设施研发
```
_块存储团队 实习_


- 观察：大数据和AI场景下，会利用块存储保存大量计算中间结果、Checkpoint 等数据。这些应用对于存储设施的吞吐有极致要求，但对于可靠性的需求可以放宽。
- 本工作利用客户端和后端存储服务器上的内存（或PMEM）对数据进行多副本存储，然后不等数据落盘即返回用户。此架构可通过在内存内积攒数据允许大比例EC和高压缩比压缩，从而在现有硬件条件下通过一个数量级的可靠性妥协达到翻倍的单机吞吐和更低的延迟。


## 发表文章

### [**Boosting File Systems Elegantly: A Transparent NVM Write-ahead Log for Disk File Systems**](https://www.usenix.org/conference/fast25/presentation/wang)

**Guoyu Wang**, Xilong Che, Haoyang Wei, Shuo Chen, Puyi He, and Juncheng Hu<br>
_In Proceedings of the 23rd USENIX Conference on File and Storage Technologies (FAST '25) (CCF A)._<br>
[[PDF](https://www.usenix.org/system/files/fast25-wang.pdf)]
[[slides](https://www.usenix.org/system/files/fast25_slides-wang.pdf)]
<!-- [[slides]({{ page.homepage.url }}/assets/plateau-19-presentation.pdf)] -->

### [**StorStack: A full-stack design for in-storage file systems**](https://www.sciencedirect.com/science/article/pii/S1383762125000207)

Juncheng Hu, Shuo Chen, Haoyang Wei, **Guoyu Wang**, Chenju Pei, and Xilong Che<br>
_Journal of Systems Architecture (CCF B)._<br>
[[PDF](https://guoyu.wang/assets/pdf/StorStack-JSA.pdf)]

## 教学与指导

技术指导，**全国计算机系统能力大赛（操作系统设计赛）全国二等奖队伍**  `吉林大学, 2024` <br>
课程规划设计（部分）, **并行与分布式计算 理论课** `吉林大学, 2023-2024` <br>
实验规划设计&助教, **并行与分布式计算 实验课** `吉林大学, 2023-2024` <br>

## 奖励和荣誉

全国商业科技进步奖一等奖 `中国商业联合会, 2023` <br>
大学生计算机系统与程序设计竞赛（CCSP） 银奖 `CCF, 2017` <br>
<!-- 校二等奖学金 `吉林大学, 2017` <br> -->

## 语言能力

**英语** CET-6 可流利交流 <br>

## Geek Moment
### **实验室网站建设** `2021`
_技能点：前端、HTML、CSS_

搭建和维护实验室网站 [jlu-ca.com](https://www.jlu-ca.com/)。

### **智能台灯** `2016`
_技能点：嵌入式、模电/数电、Android_

基于 Arduino/ESP8266 开发了自用的可联网调光调色的桌面台灯，包括电路设计、制作和控制应用程序开发。

<!-- ### Footer

Last updated: Mar 2025 -->
