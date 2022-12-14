# Chapter 6 Application layer


<!-- TOC -->

- [1. 应用层概述](#1-应用层概述)
- [2. 客户/服务器方式和对等方式](#2-客户服务器方式和对等方式)
  - [2.1. C/S方式](#21-cs方式)
  - [2.2. P2P方式](#22-p2p方式)
- [3. 动态主机配置协议DHCP](#3-动态主机配置协议dhcp)
  - [3.1. 动态主机配置协议DHCP的作用](#31-动态主机配置协议dhcp的作用)
  - [3.2. 动态主机配置协议DHCP的基本工作过程](#32-动态主机配置协议dhcp的基本工作过程)
  - [3.3. DHCP中继代理](#33-dhcp中继代理)
  - [3.4. 总结](#34-总结)
- [4. 域名系统DNS(Domain Name System)](#4-域名系统dnsdomain-name-system)
  - [4.1. 域名系统的作用](#41-域名系统的作用)
  - [4.2. 因特网的域名结构（层次树状结构）](#42-因特网的域名结构层次树状结构)
    - [4.2.1. 概述](#421-概述)
    - [4.2.2. 分类](#422-分类)
    - [4.2.3. 举例](#423-举例)
  - [4.3. 因特网上的域名服务器](#43-因特网上的域名服务器)
    - [4.3.1. 根域名服务器](#431-根域名服务器)
    - [4.3.2. 顶级域名服务器](#432-顶级域名服务器)
    - [4.3.3. 权限域名服务器](#433-权限域名服务器)
    - [4.3.4. 本地域名服务器](#434-本地域名服务器)
  - [4.4. 因特网的域名解析过程](#44-因特网的域名解析过程)
    - [4.4.1. 递归查询](#441-递归查询)
    - [4.4.2. 迭代查询](#442-迭代查询)
    - [4.4.3. 高速缓存](#443-高速缓存)
- [5. 文件传送协议FTP(File Transfer Protocol)](#5-文件传送协议ftpfile-transfer-protocol)
  - [5.1. 文件传送协议FTP的作用](#51-文件传送协议ftp的作用)
  - [5.2. 文件传送协议FTP的基本工作原理](#52-文件传送协议ftp的基本工作原理)
    - [5.2.1. 主动模式](#521-主动模式)
    - [5.2.2. 被动模式](#522-被动模式)
- [6. 电子邮件](#6-电子邮件)
  - [6.1. 电子邮件的作用](#61-电子邮件的作用)
  - [6.2. 电子邮件系统的组成](#62-电子邮件系统的组成)
    - [6.2.1. 用户代理](#621-用户代理)
    - [6.2.2. 邮件服务器](#622-邮件服务器)
    - [6.2.3. 协议](#623-协议)
  - [6.3. 简单邮件传送协议SMTP的基本工作过程](#63-简单邮件传送协议smtp的基本工作过程)
  - [6.4. 电子邮件的信息格式](#64-电子邮件的信息格式)
  - [6.5. 多用途因特网邮件扩展MIME](#65-多用途因特网邮件扩展mime)
  - [6.6. 常用的邮件读取协议（POP、IMAP）](#66-常用的邮件读取协议popimap)
  - [6.7. 基于万维网的电子邮件](#67-基于万维网的电子邮件)
- [7. 万维网WWW](#7-万维网www)
  - [7.1. 万维网概述](#71-万维网概述)
  - [7.2. 统一资源定位符URL](#72-统一资源定位符url)
  - [7.3. 万维网文档](#73-万维网文档)
  - [7.4. 超文本传输协议HTTP](#74-超文本传输协议http)
    - [7.4.1. HTTP/1.0](#741-http10)
    - [7.4.2. HTTP/1.1](#742-http11)
    - [7.4.3. HTTP报文格式](#743-http报文格式)
  - [7.5. 使用Cookie在服务器上记录信息](#75-使用cookie在服务器上记录信息)
  - [7.6. 万维网缓存与代理服务器](#76-万维网缓存与代理服务器)
- [8. 题目](#8-题目)
  - [8.1. 域名解析](#81-域名解析)
    - [8.1.1. 【2010 40】](#811-2010-40)
    - [8.1.2. 【2016 40】](#812-2016-40)
  - [8.2. FTP](#82-ftp)
    - [8.2.1. 【2009 40】](#821-2009-40)
    - [8.2.2. 【2017 40】](#822-2017-40)
  - [8.3. 电子邮件](#83-电子邮件)
    - [8.3.1. 【2012 40】](#831-2012-40)
    - [8.3.2. 【2013 40】](#832-2013-40)
    - [8.3.3. 【2018 40】](#833-2018-40)
  - [8.4. 万维网](#84-万维网)
    - [8.4.1. 【2015 40】](#841-2015-40)
    - [8.4.2. 【2011 47(3)改】](#842-2011-473改)

<!-- /TOC -->


## 1. 应用层概述

<img src="chapter-6.assets/image-20221115235645271.png" alt="image-20221115235645271" style="zoom:49%;" />

## 2. 客户/服务器方式和对等方式

### 2.1. C/S方式

<img src="chapter-6.assets/image-20221116000454896.png" alt="image-20221116000454896" style="zoom:48%;" />

### 2.2. P2P方式

<img src="chapter-6.assets/image-20221116001236513.png" alt="image-20221116001236513" style="zoom:50%;" />

## 3. 动态主机配置协议DHCP

### 3.1. 动态主机配置协议DHCP的作用

-   手动配置工作量大且容易出错

<img src="chapter-6.assets/image-20221116001810854.png" alt="image-20221116001810854" style="zoom:50%;" />

### 3.2. 动态主机配置协议DHCP的基本工作过程

<img src="chapter-6.assets/image-20221116002739123.png" alt="image-20221116002739123" style="zoom:42%;" />

### 3.3. DHCP中继代理

<img src="chapter-6.assets/image-20221116003334378.png" alt="image-20221116003334378" style="zoom:45%;" />

<img src="chapter-6.assets/image-20221116003744485.png" alt="image-20221116003744485" style="zoom:38%;" />

### 3.4. 总结

<img src="chapter-6.assets/image-20221116003839198.png" alt="image-20221116003839198" style="zoom:28%;" />

## 4. 域名系统DNS(Domain Name System)

### 4.1. 域名系统的作用

-   因特网是否可以只使用一台DNS服务器？
	-   理论可行但不可取。因为因特网的规模很大，这样的域名服务器肯定会因为超负荷而无法正常工作，而且一旦域名服务器出现故障，整个因特网就会瘫痪。

- 早在1983年，因特网就开始采用层次结构的命名树作为主机的名字（即域名），并使用分布式的域名系统DNS。
- DNS的作用
	- 系统效率高：DNS使大多数域名都在本地解析，仅少量解析需要在因特网上通信。
	- 于DNS是分布式系统，即使单个计算机出了故障，也不会妨碍整个系统的正常运行。

### 4.2. 因特网的域名结构（层次树状结构）

-   DNS报文使用运输层的UDP协议进行封装，运输层端口号为53。

#### 4.2.1. 概述

<img src="chapter-6.assets/image-20221116004816912.png" alt="image-20221116004816912" style="zoom:48%;" />

#### 4.2.2. 分类

<img src="chapter-6.assets/image-20221116004841076.png" alt="image-20221116004841076" style="zoom:47%;" />

#### 4.2.3. 举例

<img src="chapter-6.assets/image-20221116005104506.png" alt="image-20221116005104506" style="zoom:46%;" />

### 4.3. 因特网上的域名服务器
- 域名和IP地址的映射关系必须保存在域名服务器中，供所有其他应用查询。显然不能将所有信息都储存在一台域名服务器中。
- DNS使用**分布在各地的域名服务器**来**实现域名到IP地址的转换**。
#### 4.3.1. 根域名服务器

<img src="chapter-6.assets/image-20221116005518862.png" alt="image-20221116005518862" style="zoom: 48%;" />

#### 4.3.2. 顶级域名服务器

<img src="chapter-6.assets/image-20221116005548054.png" alt="image-20221116005548054" style="zoom:48%;" />


#### 4.3.3. 权限域名服务器

<img src="chapter-6.assets/image-20221116005612644.png" alt="image-20221116005612644" style="zoom:49%;" />

#### 4.3.4. 本地域名服务器

<img src="chapter-6.assets/image-20221116005637329.png" alt="image-20221116005637329" style="zoom:48%;" />

### 4.4. 因特网的域名解析过程

#### 4.4.1. 递归查询

<img src="chapter-6.assets/image-20221116010026224.png" alt="image-20221116010026224" style="zoom:50%;" />

#### 4.4.2. 迭代查询

<img src="chapter-6.assets/image-20221116010058248.png" alt="image-20221116010058248" style="zoom:46%;" />

#### 4.4.3. 高速缓存

<img src="chapter-6.assets/image-20221116010433951.png" alt="image-20221116010433951" style="zoom:45%;" />

## 5. 文件传送协议FTP(File Transfer Protocol)

### 5.1. 文件传送协议FTP的作用

<img src="chapter-6.assets/image-20221116095613892.png" alt="image-20221116095613892" style="zoom:45%;" />

- FTP的常见用途是在计算机之间传输文件，尤其是用于批量传输文件。
- FTP的另一个常见用途是让网站设计者将构成网站内容的大量文件批量上传到他们的Web服务器。
- FTP客户可向FTP服务器上传或下载文件。
- 根据应用需求的不同，FTP服务器可能
    - 需要一台高性能和高可靠性的服务器计算机，
    - 也可能只需要一台普通的个人计算机即可。

- 在windows系统中添加了一个FTP站点（FTP服务器）的方法。
    - https://www.jianshu.com/p/ece21421e246
    - https://blog.51cto.com/u_15351682/3729949

### 5.2. 文件传送协议FTP的基本工作原理

-   FTP客户和服务器之间要建立以下两个并行的TCP连接
    -   控制连接
        -   在整个会话期间**一直保持打开**，用于传送FTP相关控制命令。
    -   数据连接
        -   用于文件传输，在每次文件传输时才建立，**传输结束就关闭**。

- 默认情况下，FTP使用
    - TCP **21**端口进行**控制**连接
    - TCP **20**端口进行**数据**连接。

- 但是，**是否使用TCP 20端口建立数据连接与传输模式有关**
    - **主动方式使用TCP 20端口**
    - 被动方式由服务器和客户端自行**协商决定**。


#### 5.2.1. 主动模式

-   建立数据通道时，FTP服务器主动连接FTP客户。

<img src="chapter-6.assets/image-20221116102223536.png" alt="image-20221116102223536" style="zoom: 50%;" />

#### 5.2.2. 被动模式

- 建立数据通道时，FTP服务器被动等待FTP客户的连接。

<img src="chapter-6.assets/image-20221116101638178.png" alt="image-20221116101638178" style="zoom: 50%;" />


## 6. 电子邮件

### 6.1. 电子邮件的作用

<img src="chapter-6.assets/image-20221116102605624.png" alt="image-20221116102605624" style="zoom:44%;" />

### 6.2. 电子邮件系统的组成

-   电子邮件系统采用客户/服务器方式。

- 电子邮件系统的三个主要组成：构件用户代理，邮件服务器，以及电子邮件所需的协议

#### 6.2.1. 用户代理

-   用户与电子邮件系统的接口，又称为电子邮件客户端软件。

#### 6.2.2. 邮件服务器

-   电子邮件系统的基础设施。
-   因特网上所有的因特网服务提供者ISP都有邮件服务器，其功能是发送和接收邮件，同时还要负责维护用户的邮箱。

#### 6.2.3. 协议

- 发送协议（例如SMTP）

- 读取协议（例如POP3，IMAP）


<img src="chapter-6.assets/image-20221116102806847.png" alt="image-20221116102806847" style="zoom:44%;" />

### 6.3. 简单邮件传送协议SMTP的基本工作过程

-   Simple Mail Transfer Protocol，SMTP
    -   基于TCP连接，端口号为25。
    -   只能传送ASLII码文本。
    -   用于用户代理向邮件服务器发送邮件以及邮件服务器之间的邮件发送。


<img src="chapter-6.assets/image-20221116104230032.png" alt="image-20221116104230032" style="zoom:41%;" />

### 6.4. 电子邮件的信息格式

-   信封
-   内容
    -   首部
    -   主体

<img src="chapter-6.assets/image-20221116104435572.png" alt="image-20221116104435572" style="zoom:44%;" />

### 6.5. 多用途因特网邮件扩展MIME

- 为解决SMTP传送非ASCII码文本的问题，提出MIME。
- 多用途因特网邮件扩展 (Multipurpose Internet Mail Extensions，MIME)
    - 增加了5个新的邮件首部字段，这些字段提供了有关邮件主体的信息。
    - 定义了许多邮件内容的格式，对多媒体电子邮件的表示方法进行了标准化。定义了传送编码，可对任何内容格式进行转换，而不会被邮件系统改变
    - 定义了传送编码，可对任何内容格式进行转换，而不会被邮件系统改变。
- MIME不仅仅用于SMTP，也用于后来的同样面向ASCII字符的HTTP。

<img src="chapter-6.assets/image-20221116113335844.png" alt="image-20221116113335844" style="zoom:45%;" />

### 6.6. 常用的邮件读取协议（POP、IMAP）

<img src="chapter-6.assets/image-20221116105139934.png" alt="image-20221116105139934" style="zoom:45%;" />

### 6.7. 基于万维网的电子邮件

- 通过浏览器登录（提供用户名和口令）邮件服务器万维网网站就可以撰写、收发、阅读和管理电子邮件。
- 这种工作模式与IMAP很类似，**不同**的是**用户计算机无需安装专门的用户代理程序**，只需要使用用的万维网浏览器。
    - 用户浏览器与邮件服务器网站之间使用 HTTP协议
    - 邮件服务器之间使用 SMTP协议。

- 邮件服务器网站通常都提供非常强大和方便的邮件管理功能，用户可以在邮件服务器网站上管理和处理自己的邮件，而不需要将邮件下载到本地进行管理。

<img src="chapter-6.assets/image-20221116110142584.png" alt="image-20221116110142584" style="zoom:41%;" />

## 7. 万维网WWW

### 7.1. 万维网概述

- 万维网（World Wide Web，WWW）**并非某种特殊的计算机网络**。它是一个大规模的、联机式的信息储藏所，**是运行在因特网上的一个分布式应用**。
- 万维网利用网页之间的**超链接**将不同网站的网页链接成一张逻辑上的信息网。
- 浏览器最重要的部分是**渲染引擎**，也就是**浏览器内核**。负责对网页内容进行解析和显示。
    - 不同的浏览器内核对网页内容的解析也有不同，因此同一网页在不同内核的浏览器里的显示效果可能不同；
    - 网页编写者需要在不同内核的浏览器中测试网页显示效果。


<img src="chapter-6.assets/image-20221116120950142.png" alt="image-20221116120950142" style="zoom:50%;" />

### 7.2. 统一资源定位符URL

-   Uniform Resource Locator
	-   指明因特网上任何种类“资源”的位置。
	-   可以方便地访问在世界范围的文档。

<img src="chapter-6.assets/image-20221116121545866.png" alt="image-20221116121545866" style="zoom: 33%;" />

### 7.3. 万维网文档

<img src="chapter-6.assets/image-20221116121850556.png" alt="image-20221116121850556" style="zoom:46%;" />

### 7.4. 超文本传输协议HTTP

-   HyperText Transfer Protocol
	-   HTTP定义了浏览器（即万维网客户进程）怎样向万维网服务器请求万维网文档，以及万维网服务器怎样把万维网文档传送给浏览器。

<img src="chapter-6.assets/image-20221116132935629.png" alt="image-20221116132935629" style="zoom:40%;" />

#### 7.4.1. HTTP/1.0

-   非持续连接：每次浏览器要请求一个文件都要与服务器建立TCP连接，当收到响应后就立即关闭连接。
	-   每请求一个文档就要有两倍的RTT的开销。若一个网页上有很多引用对象（例如图片等），那么请求每一个对象都需要花费2RTT的时间。
	-   为了减小时延，浏览器通常会**建立多个并行的TCP连接同时请求多个对象**。但是，这会**大量占用万维网服务器的资源**，特别是万维网服务器往往要同时服务于大量客户的请求，这会使其负担很重。

<img src="chapter-6.assets/image-20221116133353301.png" alt="image-20221116133353301" style="zoom:40%;" />

#### 7.4.2. HTTP/1.1

-   持续连接：万维网服务器在**发送响应后仍然保持这条连接**，使同一个客户（浏览器）和该服务器可以继续在这条连接上传送后续的HTTP请求报文和响应报文。这并不局限于传送同一个页面上引用的对象，而是只要这些文档都在同一个服务器上就行。
	-   为了进一步提高效率，HTTP/1.1的持续连接还可以使用**流水线**方式工作，即浏览器在收到HTTP的响应报文之前就能够连续发送多个请求报文。这样的一个接一个的请求报文到达服务器后，服务器就发回一个接一个的响应报文。这样就节省了很多个RTT时间，使TCP连接中的空闲时间减少，提高了下载文档的效率。

#### 7.4.3. HTTP报文格式

-   HTTP是**面向文本**的，其报文中的每一个**字段**都是一些**ASCII码串**，并且每个字段的**长度都是不确定**的。

-   请求报文格式
    -   判断是否为持续连接要看报文中Connection的值，close为非持续连接，keep-alive为非持续连接；而不能只是看HTTP版本号。


<img src="chapter-6.assets/image-20221116134558329.png" alt="image-20221116134558329" style="zoom:45%;" />

-   响应报文格式

<img src="chapter-6.assets/image-20221116134923312.png" alt="image-20221116134923312" style="zoom:42%;" />

### 7.5. 使用Cookie在服务器上记录信息

-   早期用户在万维网上仅查看存放在不同服务器上的各种静态文档。
-   HTTP被设计为一种无状态的协议。
-   Cookie是一种对无状态的HTTP进行状态化的技术，提供了一种机制使万维网服务器能够“记住”用户。

<img src="chapter-6.assets/image-20221116135530105.png" alt="image-20221116135530105" style="zoom:42%;" />

### 7.6. 万维网缓存与代理服务器

-   万维网中可以使用缓存机制以提高万维网的效率。
-   万维网缓存又称为**Web缓存（Web Cache）**，可位于客户机，也可位于中间系统上，**位于中间系统上的Web缓存又称为代理服务器（Proxy Server）**。
-   Web缓存把最近的一些请求和响应暂存在本地磁盘中。当新请求到达时，若发现这个请求与暂时存放的请求相同，就返回暂存的响应，而不需要按URL的地址再次去因特网访问该资源。
	-   若Web缓存的命中率比较高，则大大减少了该链路上的通信量因而减少了访问因特网的时延。
	-   代理服务器会给每一个响应对象设定一个修改时间字段（Last-Modified）和有效时间字段（Expires）
		-   若有效时间过期，代理服务器会给原始服务器发送包含if-modified-since的请求，原始服务器通过文档修改日期的对比就可判断出代理服务器的文档是否与当前文档一致。
			-   一致，发回304 Not Modified响应，代理服务器更新文档有效日期，封装在响应报文中发回主机。
			-   不一致，发回封装新文档的响应报文，代理服务器再将该文档封装再响应报文中发回主机。

<img src="chapter-6.assets/image-20221116140909146.png" alt="image-20221116140909146" style="zoom:50%;" />

## 8. 题目

### 8.1. 域名解析

#### 8.1.1. 【2010 40】

<img src="chapter-6.assets/image-20221116011221785.png" alt="image-20221116011221785" style="zoom:45%;" />

#### 8.1.2. 【2016 40】

<img src="chapter-6.assets/image-20221116011933628.png" alt="image-20221116011933628" style="zoom:40%;" />

### 8.2. FTP

#### 8.2.1. 【2009 40】

<img src="chapter-6.assets/image-20221116101848741.png" alt="image-20221116101848741" style="zoom:44%;" />

#### 8.2.2. 【2017 40】

<img src="chapter-6.assets/image-20221116101832366.png" alt="image-20221116101832366" style="zoom:44%;" />

### 8.3. 电子邮件

#### 8.3.1. 【2012 40】

<img src="chapter-6.assets/image-20221116105840121.png" alt="image-20221116105840121" style="zoom:41%;" />

#### 8.3.2. 【2013 40】

<img src="chapter-6.assets/image-20221116113645104.png" alt="image-20221116113645104" style="zoom:43%;" />

#### 8.3.3. 【2018 40】

<img src="chapter-6.assets/image-20221116113717995.png" alt="image-20221116113717995" style="zoom:50%;" />

### 8.4. 万维网

#### 8.4.1. 【2015 40】

<img src="chapter-6.assets/image-20221116141454606.png" alt="image-20221116141454606" style="zoom:43%;" />

#### 8.4.2. 【2011 47(3)改】

<img src="chapter-6.assets/image-20221116141605586.png" alt="image-20221116141605586" style="zoom:41%;" />
