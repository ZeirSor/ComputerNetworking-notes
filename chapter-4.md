#  Chapter 4 Network layer

## 网络层概述



## 网际协议IP



### 异构网络互连



### IPv4地址及其编址方法

#### 分类编制方法



#### 划分子网的编址方法



#### 无分类编址方法



### IPv4地址的应用规划



### IPv4地址与MAC地址



### 地址解析协议ARP



### IP数据报的发送和转发流程



### IPv4数据报的首部格式



## 静态路由配置

### 因特网的路由选择协议



### 路由信息协议RIP



### 开放最短路径优先OSPF



### 边界网关协议BGP



### 路由器的基本工作原理



## 网际控制协议ICMP



## 虚拟专用网VPN和网络地址转换NAT



## IP多播技术

### 相关基本概念

### IP多播地址和多播组

### 在局域网上进行硬件多播

### 在因特网上进行IP多播需要的两种协议

### 网际组管理协议IGMP

### 多播路由选择协议

## 移动IP技术概述

## IPv6

### IPv6的诞生背景

- IPv4地址存在缺陷
    - IPv4地址的长度仅为32比特
    - 早期的编址方法不够合理，造成IPv4地址资源的浪费。

- 2011年2月3日，因特网号码分配管理局IANA宣布IPv4地址已经分配完毕
- 如果没有网络地址转换NAT技术的广泛应用，IPv4早已停止发展。
- 解决IPv4地址耗尽的根本措施就是采用具有更大地址空间（IP地址的长度为128比特）的新版本IP，即IPv6。
- 到目前为止，IPv6还只是草案标准阶段

- 尽早开始过渡到IPv6的好处
	- 有更多时间来平滑过渡
	- 有更多时间来培养IPv6的专门人才
	- 及早提供IPv6服务比较便宜

### IPv6引进的主要变化

<img src="chapter-4.assets/image-20221113115313786.png" alt="image-20221113115313786" style="zoom:33%;" />

### IPv6数据包的基本首部

<img src="chapter-4.assets/image-20221113115233928.png" alt="image-20221113115233928" style="zoom: 30%;" />

### IPv6数据包的扩展首部

<img src="chapter-4.assets/image-20221113115857414.png" alt="image-20221113115857414" style="zoom: 50%;" />

### IPv6地址

#### IPv6地址空间大小

<img src="chapter-4.assets/image-20221113120034870.png" alt="image-20221113120034870" style="zoom:50%;" />

#### IPv6地址的表示方法

<img src="chapter-4.assets/image-20221113132938404.png" alt="image-20221113132938404" style="zoom:33%;" />

<img src="chapter-4.assets/image-20221113133637060.png" alt="image-20221113133637060" style="zoom:33%;" />

<img src="chapter-4.assets/image-20221113133657175.png" alt="image-20221113133657175" style="zoom:33%;" />

<img src="chapter-4.assets/image-20221113133713447.png" alt="image-20221113133713447" style="zoom:43%;" />

#### IPv6地址的分类

<img src="chapter-4.assets/image-20221113133959853.png" alt="image-20221113133959853" style="zoom:33%;" />

<img src="chapter-4.assets/image-20221113134227184.png" alt="image-20221113134227184" style="zoom:41%;" />

### 从IPv4向IPv6过渡

- 因特网上使用IPv4的路由器的数量太大，要让所有路由器都改用IPv6并不能一蹴而就。因此，从IPv4转变到IPv6只能采用**逐步演进**的办法。
- 另外，**新部署的IPv6系统必须能够向后兼容**，也就是IPv6系统必须能够接收和转发IPv4数据报，并且能够为IPv4数据报选择路由。

#### 使用双协议栈
- 双协议栈（Dual Stack）是指在完全过渡到IPv6之前，使一部分主机或路由器装有IPv4和IPv6两套协议栈。
- 双协议栈主机或路由器既可以和IPv6系统通信，又可以和IPv4系统通信。
- 双协议栈主机或路由器记为IPv6/IPv4，表明它具有一个IPv6地址和一个IPv4地址。
	- 双协议栈主机在与IPv6主机通信时采用IPv6地址，而与IPv4主机通信时采用IPv4地址
	- 双协议栈主机通过域名系统DNS查询目的主机采用的IP地址：
		- 若DNS返回的是IPv4地址，则双协议栈的源主机就使用IPv4地址
		- 若DNS返回的是IPv6地址，则双协议栈的源主机就使用IPv6地址

<img src="chapter-4.assets/image-20221113140501907.png" alt="image-20221113140501907" style="zoom:33%;" />

#### 使用隧道技术

- 隧道技术（Tunneling）的核心思想是：
	- 当IPv6数据报要进入IPv4网络时，将IPv6数据报重新封装成IPv4数据报，即整个IPv6数据报成为IPv4数据报的数据载荷。
	- 封装有IPv6数据报的IPv4数据报在IPv4网络中传输。
	- 当IPv4数据报要离开IPv4网络时，再将其数据载荷（即原来的IPv6数据报）取出并转发到IPv6网络。

<img src="chapter-4.assets/image-20221113140813293.png" alt="image-20221113140813293" style="zoom:33%;" />

### 网际控制报文协议ICMPv6

#### 概述

<img src="chapter-4.assets/image-20221113141017941.png" alt="image-20221113141017941" style="zoom:33%;" />

#### ICMPv6报文的封装

<img src="chapter-4.assets/image-20221113141253442.png" alt="image-20221113141253442" style="zoom:25%;" />

#### ICMPv6报文的分类

<img src="chapter-4.assets/image-20221113141259414.png" alt="image-20221113141259414" style="zoom:25%;" />

## 软件定义网络SDN

	### 概述

<img src="chapter-4.assets/image-20221113153015457.png" alt="image-20221113153015457" style="zoom: 50%;" />

### 网络层的数据层面和控制层面

<img src="chapter-4.assets/image-20221113153342923.png" alt="image-20221113153342923" style="zoom:41%;" />

### OpenFlow协议

#### 概述

<img src="chapter-4.assets/image-20221113153540950.png" alt="image-20221113153540950" style="zoom:50%;" />

<img src="chapter-4.assets/image-20221113153621464.png" alt="image-20221113153621464" style="zoom:45%;" />

#### 传统意义上的数据层面的任务

<img src="chapter-4.assets/image-20221113153755626.png" alt="image-20221113153755626" style="zoom:40%;" />

#### SDN中的广义转发

<img src="chapter-4.assets/image-20221113153820417.png" alt="image-20221113153820417" style="zoom:25%;" />

#### OpenFLow交换机和流表

<img src="chapter-4.assets/image-20221113153925991.png" alt="image-20221113153925991" style="zoom:33%;" />

<img src="chapter-4.assets/image-20221113154436668.png" alt="image-20221113154436668" style="zoom:55%;" />

-   简单转发

<img src="chapter-4.assets/image-20221113154544128.png" alt="image-20221113154544128" style="zoom:45%;" />

-   负载均衡

<img src="chapter-4.assets/image-20221113154608415.png" alt="image-20221113154608415" style="zoom:50%;" />

-   防火墙

<img src="chapter-4.assets/image-20221113154653434.png" alt="image-20221113154653434" style="zoom:49%;" />

### SDN体系结构

#### SDN体系结构及其四个关键特征

-   基于流的转发
-   数据层面与控制层面分离
-   位于数据层面分组交换机之外的网络控制功能
-   可编程的网络

#### SDN控制器

<img src="chapter-4.assets/image-20221113155239475.png" alt="image-20221113155239475" style="zoom:30%;" />

### 总结

<img src="chapter-4.assets/image-20221113155508746.png" alt="image-20221113155508746" style="zoom: 27%;" />

### SDN题目

<img src="chapter-4.assets/image-20221113155414924.png" alt="image-20221113155414924" style="zoom:26%;" />
