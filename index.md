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

### **利用 NVM 高效、优雅、透明地加速磁盘存储堆栈** 
_技能点：内核开发、C语言、NVM优化、文件系统设计、一致性算法、模型检查、TLA+_

- 核心洞察：磁盘文件系统只有在DRAM缓存不起效（同步写/缓存未命中）时需要磁盘IO，性能较低。其余情况下磁盘文件系统性能高于NVM文件系统。
- 工作内容：在内核VFS层拦截同步调用并记录到NVM上，在崩溃后对未写回磁盘的同步写入进行重放，从而让磁盘文件系统精准绕过缓慢的前台磁盘IO路径，达到透明加速。
- 本工作部分成果已发表在 **FAST '25**，为吉林大学在系统和存储领域首篇顶会文章。


## 专业经历

### **阿里云** `2025.5 - 2025.8`
```
面向高吞吐场景的下一代互联网存储设施研发
```
_块存储团队 实习_


- 核心洞察：大数据和AI场景下，会利用块存储保存大量计算中间结果、Checkpoint 等数据。这些应用对于存储设施的吞吐有极致要求，但对于可靠性的需求可以放宽。
- 工作内容：利用客户端和后端存储服务器上的内存（或PMEM）对数据进行多副本存储，然后不等数据落盘即返回用户。此架构可通过在内存内积攒数据允许大比例EC和高压缩比压缩，从而在现有硬件条件下通过一个数量级的可靠性妥协达到翻倍的单机吞吐和更低的延迟。


## 发表文章

### [**Boosting File Systems Elegantly: A Transparent NVM Write-ahead Log for Disk File Systems**](https://www.usenix.org/conference/fast25/presentation/wang)

**Guoyu Wang**, Xilong Che, Haoyang Wei, Shuo Chen, Puyi He, and Juncheng Hu<br>
_In Proceedings of the 23rd USENIX Conference on File and Storage Technologies (FAST '25) (CCF A)._<br>
[[PDF](https://www.usenix.org/system/files/fast25-wang.pdf)]
[[slides](https://www.usenix.org/system/files/fast25_slides-wang.pdf)]
<!-- [[slides]({{ page.homepage.url }}/assets/plateau-19-presentation.pdf)] -->

### **A Transparent NVM Acceleration Framework for Disk File Systems**
**Guoyu Wang**, Juncheng Hu, Can Zhou, Haoyang Wei, Chenju Pei, Puyi He, Tengfei Li, and Xilong Che<br>
_ACM Transactions on Storage (TOS) (CCF A)._<br>

### [**StorStack: A full-stack design for in-storage file systems**](https://www.sciencedirect.com/science/article/pii/S1383762125000207)

Juncheng Hu, Shuo Chen, Haoyang Wei, **Guoyu Wang**, Chenju Pei, and Xilong Che<br>
_Journal of Systems Architecture (CCF B)._<br>
[[PDF](https://guoyu.wang/assets/pdf/StorStack-JSA.pdf)]

## 教学与指导

技术指导，**全国计算机系统能力大赛（操作系统设计赛）全国二等奖队伍**  `吉林大学, 2024` <br>
课程规划设计（部分）, **并行与分布式计算 理论课** `吉林大学, 2023-2024` <br>
实验规划设计&助教, **并行与分布式计算 实验课** `吉林大学, 2023-2024` <br>

## 奖励和荣誉

中国存储大会最佳论文海报奖 `CCF, 2025` <br>
全国商业科技进步奖一等奖 `中国商业联合会, 2023` <br>
大学生计算机系统与程序设计竞赛（CCSP） 银奖 `CCF, 2017` <br>
<!-- 校二等奖学金 `吉林大学, 2017` <br> -->

## 语言能力

**英语** CET-6 可流利交流 <br>

<!-- ## Geek Moment
### **实验室网站建设** `2021`
_技能点：前端、HTML、CSS_

搭建和维护实验室网站 [jlu-ca.com](https://www.jlu-ca.com/)。

### **智能台灯** `2016`
_技能点：嵌入式、模电/数电、Android_

基于 Arduino/ESP8266 开发了自用的可联网调光调色的桌面台灯，包括电路设计、制作和控制应用程序开发。 -->

<!-- ### Footer

Last updated: Mar 2025 -->
