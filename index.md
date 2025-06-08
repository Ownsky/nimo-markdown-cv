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

### **利用 NVM 高效、透明地加速磁盘文件系统** 
_技能点：内核开发、C语言、NVM优化、文件系统设计_

- 观察：在缓存命中的情况下，只有在进行持续的同步写入时，NVM 文件系统性能才优于 DRAM cache。然而大部分应用以读取和异步写入为主，同步写入仅偶尔出现成为性能瓶颈。因此，NVM 文件系统仅适用于写密集 DB 这类场景，对于其他任务 DRAM cache 收益更高。
- 本工作提出 NVLog，拟在*保留 DRAM cache* 性能优势的基础上*利用 NVM* 的高速持久化特性，通过*选择性吸收同步写入*来精准绕过缓慢的磁盘 IO 路径。NVLog 被设计为在 VFS 层内部拦截并记录同步调用的 WAL，保持了对上层应用和底层 FS 的透明。相比其他工作，NVLog 可以提供更高的运行效率（精准吸收&无索引）和更低的 NVM 空间占用（日志可回收）。
<!-- - 选择性吸收同步写入可能造成磁盘、NVM数据版本不一致的问题。本工作通过在NVM上建立全局时钟来解决 _崩溃一致性_ 问题。此外本工作还提供主动同步机制缓解fsync调用下分散小写入可能造成的写入放大问题。 -->
- 本工作成果已发表在 **FAST '25**。



### **探究混合异构存储系统中的一致性问题（进行中）** 
_技能点：一致性算法、模型检查、TLA+_

- 以“同步”操作为切入点，给出崩溃一致性的形式化定义，基于此探究 DRAM、NVM、磁盘混合异构存储系统中可能存在的*一致性问题*，并给出解决办法。
- 使用*形式化验证（模型检查）*方法证明所提出方案的正确性。鉴于模型检查方法会生成无限状态空间，拟分析任务内在逻辑并提供规约，将状态空间限制在有穷集合内，同时保证有穷空间下的正确性可推广至无穷空间。


<!-- ## 研究兴趣
- 操作系统
- 存储系统、文件系统
- 分布式系统 -->

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
[[PDF]({{ page.homepage.url }}/assets/pdf/StorStack-JSA.pdf)]

## 教学与指导

技术指导，**全国计算机系统能力大赛（操作系统设计赛）全国二等奖队伍**  `吉林大学, 2024` <br>
课程设计（部分）, **并行与分布式计算 理论课** `吉林大学, 2023-2024` <br>
实验设计&助教, **并行与分布式计算 实验课** `吉林大学, 2023-2024` <br>



## 奖励和荣誉

全国商业科技进步奖一等奖 `中国商业联合会, 2023` <br>
大学生计算机系统与程序设计竞赛（CCSP） 银奖 `CCF, 2017` <br>
<!-- 校二等奖学金 `吉林大学, 2017` <br> -->

## 语言能力

**英语** CET-6 可流利交流 <br>

## Geek Moment
### **实验室网站建设** `2021`
_技能点：前端、HTML、CSS_

搭建和维护实验室网站 [jlu-ca.com](https://www.jlu-ca.com/)。网站使用主题与内容解耦的[Hexo](https://hexo.io/)静态博客框架开发。主题基于[Pure](https://github.com/cofess/hexo-theme-pure)进行深度改造以适配实验室需求。

### **寝室智能台灯** `2016`
_技能点：嵌入式、模电/数电、Android_

基于 Arduino/ESP8266 开发了自用的可联网调光调色的桌面台灯。同时设计并制作了整个电路部分，以及开发了配套的安卓控制应用。

<!-- ### Footer

Last updated: Mar 2025 -->
