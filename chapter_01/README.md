# 计算机网络和因特网

- **按媒介来区分**
  组成网络的端到端,包括笔记本电脑,智能手机,甚至汽车,体重计
- **按抽象来区分**
  软件和硬件,再细分可能是浏览器,网卡驱动与路由器网线
- **按前端-后端来区分**

## 前端的趋势

当然不是说的前端技术, 前端以电脑为主,前端以手机为主,前端以物联网为主(体温计,温度计,体重计,甚至空调),据估计,到 2015 为止,全球超过`5B`台设备连接网络,超过`3B`用户,

## 通讯链路 与 交换机

端系统依靠不同的`通讯链路`和`交换机`连接到一起.

- **通讯链路**可以是`光纤`,`铜线`,`WiFi/无限电频谱`,当一个端系统要向另一个端系统发送数据,发送端系统将数据`分组`,分成不同的数据包,每个包加上首部字节,等到了目标机器,再被装配组成初始数据.
- **分组交换机**从它的一条入通讯链路接收到分组.并将它的一条出通信链路转发该分组,如今市场最流行的`路由器`-位于网络核心中,`链路层交换机`-常用语接入网络中.

## 目前全球 IP 流量超过 ZB(zettabyte)

- Bit - 比特,二进制某位数
- Byte - 字节, 8 个比特构成, 0000 0000 ,可构成一个 ASCII 标准单词[a-zA-Z],2 个字节构成一个汉字
- KB kilobyte - 1024 2^10 个字节
- MB Million byte 兆
- GB gigabyte 一部电影
- TB trillionbyte 某个大硬盘
- PB Petabyte 阿里巴巴存储的支付宝用户数据总和 peta kill 五杀
- EB exabyte
- ZB zettabyte 全球一年的流量
- YB yottabyte
- BB Brontobyte

## 网络协议 - 物流系统 区别

一个传输数据,一个传输实体包裹,他们的共同点是协议以及传输方式,物流公司想要将大批量货物运输给远方,一次运不完,分开一车车运输,途径高速公路,国道凹凸不平,交叉口,到达目的地后,货物以约定的头部拼接 index,进行摆放.

## ISP 因特网服务供应商 Internet Service Provider

端系统通过 ISP 接入英特网,,其中包括住宅 ISP,公司 ISP,机场 ISP,大学,旅馆 ISP,或者其他公共场所提供的 wifi 接入的 ISP,还有智能手机连接的蜂窝网络 ISP,每个 ISP 自身就是一个由多台分组交换机和多段通讯链路组成的网络,各个 ISP 为端系统提供了不同的网络接入,如线缆调试解调器,或者 DSL 那样的生活宽带接入,高速局域网接入,移动无线网络接入,ISP 同样为终端提供接入,所以说,ISP 就是为互联网中的端到端实现互联,同样,ISP 彼此也可以互联,底层 ISP 和国家的,国际的高级 ISP 互联,高层 ISP 通过高速光纤,以及高速路由器组成.

## TCP 与 IP 协议

端系统,分组交换机,其他网络部件都运行一套**协议**,

- **TCP**(Transmission Control Protocol, 传输控制协议)
- **IP**(Internet Protocal 网际协议) 定义了在路由器和端系统之间发送接受的分组格式.

## 协议

定义了在两个或者多个通讯实体之间交换的报文的格式和顺序,以及报文发送和/接收一条报文或其他事件所采取的动作.

## 网络边缘

端系统,前端/服务端

## 接入网

即将端系统物理连接到其边缘路由器的网络

- 家庭接入: DSL, 电缆, FTTH, 拨号和卫星 🛰,而今天最流行的宽带住宅接入类型: **数字用户线 DSL(DIgital Subscriber Line)** 和 **电缆**,

## DSL 标准

定义了多种传输速率, 分别对应不同价格

- 12Mbps 下行和 1.8Mbps 上行传输速率[ITU 1999]
- 55Mbps 下行和 15Mbps 上行传输速率[ITU 2006]

## 光纤到户(Fiber To The Home, FTTH)

即从本地中心局直接到用户家提供了条光纤路径,

## 企业和家庭的接入: 以太网和 WIFI

在大公司和在大学校园.越来越多的家庭环境中,使用局域网(LAN)将端系统连接到边缘路由器,目前为止以太网是最流行的技术,一般以 100Mbps 或者 1Gbps 速率接入以太网交换机网络.一种是无线 LAN,用户必须站在 100 米范围内.而基于`IEEE802.11`技术的无限 LAN 接入技术,就是如今的 wifi,他几乎无处不在,Starbucks,机场,办公室,家庭,甚至飞机上,`802.11`今天一般提供了`100Mbps`的共享传出速率.

## 广域无线接入: 3G 和 LTE

就是无线流量,与 WiFi 不同,一个用户需要与自己相距数万米范围的基站相连接.

## 1.2.2 物理媒介

一个比特-byte 从一个端系统开始,通过一系列链路和路由器,到达另一个端系统,byte 被漫不经心的传输了很多次,端原系统发射这个比特,不久后,被第一个路由器接受,他再把这个比特发射出去,到第二个路由器,局域网依靠广播形式找到真正的服务器,而互联网则依靠路由器进行数据发送,这个 byte 经历了一系列`emit-receive`,每次`emit-receive`都会跨越一个**物理媒介**,

### 物理媒介分类

导引型媒介网线铜线

#### 双绞铜线

两根绝缘铜线构成,10Mbps-10Gbps,取决于发射接收双方网速,铜线长度,粗度,目前主流,

#### 同轴电缆

两根铜导体构成,通常作为电视电缆

#### 光纤

柔软细腻,能够引导光脉冲的媒体,每个脉冲表示一个比特,即最小的二进制单位,一根光纤支持极高的比特速率,高达 10Gbps,不受到电磁干扰,

### 非导引型媒介

无限局域网,无线 WiFi

## 1.3 网络核心

### 1.3.1 分组交换机

各种网络应用中,端系统彼此交换**报文**,包含设计者需要的任何东西,将报文分割成较小数据,称之为**分组**,源和目的地之间,分为较小的数据块,每个分组经过通信链路和分组交换机,交换机主要分为**路由器**,**链路层交换机**

#### 1.存储转发传输

多数分组交换机在链路的输入端使用**存储转发传输**机制,存储转发传输指的 交换机能开始向链路传输该分组的第一个比特之前,必须接受到整个分组,每台路由器通常有多个繁忙链路,路由器的任务就是将一个人分组交换到一跳出链路,

#### 2.排队延时和分组丢失

每台分组交换机有多条链路与之相连,对于每条相连的链路,该分组交换机具有一个**输出缓存**,也称之为**输出队列**.如果到达的分组忙于传输其他分组,该到达分组必须在输出缓存中等待,这就是**排队延迟**.而缓存是有限的,一旦满了,就**分组丢包**.

#### 3.转发表和路由选择协议

路由从与他相连的一条通讯线路获得**分组**,向与它相连的另一条通讯链路转发该分组,路由应该怎样决定他该向哪条链路进行转发呢,不同的计算机网络以不同的规则转发,事实上,每台路由器有一个**转发表**,分组首部包含了`IP`,通过转发表,将目标地址映射成输出链路,转发表如何进行设置,是通过人工为每一台路由器设置,还是从网络上获取,实际上`internal`上有一些特殊的`路由选择协议`,用于自动的设置这些转发表.路由选择协议可以决定最短到达路径.并从最短路径结果来配置路由器中的转发表.

### 1.3.2 电路交换

通过网络链路和交换机移动数据有两种基本方法, **电路交换** 和 **分组交换**,下面介绍电路交换,