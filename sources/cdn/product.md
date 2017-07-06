##产品概述

又拍云 CDN ( Content Delivery Network，内容分发网络 ) 服务是遍布全球的内容分发网络。内容分发网络是一种通过部署在互联网上的高度分布式的加速平台，代替了传统以 `Web Server` 为中心的数据传输模式，可直接响应最终用户（ 也即客户端 ）的 Web 内容请求。通过内容分发网络，可将网站的静态资源，如图片、JavaScript  、CSS、网页等内容发布到最接近最终用户（ 客户端 ）的网络边缘  ，配合精准智能调度和边缘缓存，使得最终用户都能够快速安全可靠的访问到网站资源，以确保最终用户得到最快的页面加载时间和最佳的性能。与此同时，可大幅降低源站压力。

又拍云内容分发网络结合优质的网络节点资源、网络服务器技术以及传输路由技术优势，构建了下一代 CDN 加速平台。我们的服务器软件可有效处理每秒百万次的请求，我们力求让 CDN 服务更加简单、高效、安全，尽一切可能帮助用户解决互联网上可能影响数据传输速度和稳定性的瓶颈和环节。


假设您的业务访问域名为 `www.abc.com`，当该域名接入到又拍 CDN 服务之后，您的最终用户发起的 HTTP 请求，实际的访问流程如下图所示：

![upyun-cdn-dns-theory](http://upyun-assets.b0.upaiyun.com/docs/cdn/product-introduction/upyun-cdn-dns-theory.jpg_/fw/830)


----------


##产品架构

整个产品架构由客户端、CDN 网络、企业源站、管理控制台、CDN 智能调度系统等角色及模块组成。产品架构如下图所示：

![ upyun-cdn-architecture ](http://upyun-assets.b0.upaiyun.com/docs/cdn/product-introduction/upyun-cdn-architecture.png_/fw/830)

**客户端**

客户端通过 DNS 解析可以快速接入到又拍云 CDN 网络，CDN 智能调度系统可以响应一个离用户最近的 CDN 边缘节点 IP 给客户端，客户端可以达到就近访问的目的。

**CDN 网络**

又拍云 CDN 网络由边缘节点集群、中心节点集群、智能调度系统等模块和基础设施组成。节点集群除了具备高性能的缓存设备，还具备四层和七层的负载均衡功能。

**企业源站**

企业源站可以是企业自建的源站或者托管在第三方存储的静态资源，CDN 网络作为反向代理会根据客户端的请求回源站请求资源文件并将数据资源进行缓存。

**管理控制台**

用户可通过又拍云管理控制台、API 的方式，管理托管在又拍云 CDN 网络上的资源及服务，通过更多的统计数据展示，使得 CDN 服务更加方便、快捷。


----------


##主要功能

| 功能类别 | 功能名称      |    详细     |  是否支持 | 
|---------------------|------------------------|------------------|------------|
|   服务管理   | 管理方式    | 支持管理控制台图形化管理、API 管理 |  √  | 
|           |  API 管理      | 支持创建、修改、删除、启用、停止服务，统计分析及日志下载等   |   √  | 
|           |  域名绑定     | 一个服务下最多可以绑定 10 个域名，支持泛域名，不支持未备案域名|   √   | 
| 内容管理   |  缓存配置 | 支持自定义缓存时间设置，可针对文件后缀、目录等进行资源缓存时间的设置                  |   √  | 
|            |   内容刷新   | 支持 URL 刷新以及规则刷新，可将 CDN 节点的文件进行删除或致过期处理|   √   | 
|             |  URL 预热     | 可将热门文件提前缓存至 CDN 节点，降低源站压力|   √  | 
|             |  参数跟随     | 控制是否过滤请求中的查询字符串，支持忽略参数、全程跟随、回源跟随等模式|   √  | 
|  访问控制    |  黑白名单     | 支持 IP、URL 黑白名单设置，禁用非法资源访问|   √   | 
|              |  防盗链     | 支持地区访问限制、Token、Referer、回源鉴权等多种防盗链方式|   √   | 
|              |  WAF 防护     | 能有效拦截跨站攻击、SQL 注入和其他代码执行等多种攻击方式|   √  | 
|              |  CC 防护    | 可有效防止 DDos  攻击中的 CC 攻击，支持智能及强制防护模式|   √   | 
|           |  HTTP请求大小限制   | 可限制单次请求体的内容大小，能有效保证请求的安全性|   √  | 
|  统计分析    |  带宽统计     | 可根据地区、运营商等维度查看域名及服务最近 30 天的带宽趋势及详细统计数据|   √  | 
|              |  流量统计     | 可根据地区、运营商等维度查看域名及服务最近 30 天的流量趋势及详细统计数据|   √  | 
|              |  请求数统计     | 可根据地区、运营商等维度查看域名及服务最近 30 天的请求数趋势及详细统计数据|   √   | 
|               |  导出历史数据     | 可根据地区、运营商等维度查看域名及服务最近 30天 5分钟粒度的详细带宽数据|   √  | 
|  性能监控    |  健康度     | 统计所有请求的 HTTP 状态码，计算 2xx 和 3xx 请求次数所占的比例|   √  | 
|               |  缓存命中率     | 统计所有请求数中，命中缓存的请求数所占的比例|  √    | 
|               |  平均下载速度     | 可以根据地区和运营商来区分资源文件下载速度和请求耗时|   √  | 
|               |  拦截攻击次数     | 拦截的跨站攻击、SQL 注入和其他代码执行等多种攻击的数量 |   √   | 
|  高级服务    |  自定义 SSL 服务     | 用户可以上传自己的 SSL 证书到又拍云，并管理自定义域名的 HTTPS 访问|   √   | 
|               |  视频拖拉     | 支持 MP4，FLV 文 件根据视频头进行拖拉播放，默认 MP4 按时间拖拉，FLV 按字节拖拉|   √   | 
|               |  CORS 跨域共享    | 用户可以在又拍云控制台配置符合自己站点的跨域请求策略|   √  | 
|                |  自定义 Rewrite     | 用户可以根据系统预设函数、请求变量及字符串常量等进行自由组合，完成对请求的重写|   √  | 
|                 |  自定义提示图     | 可以根据 403、404、405 等状态码进行自定义提示图的设置|   √   | 
|                 |  镜像存储     | 支持将第三方存储以及企业源站的静态资源通过镜像的方式逐步迁移到又拍云存储|   √  | 
|  日志管理       |  日志下载    | 支持以小时粒度的日志下载，可收集详细的终端访问日志|   √   | 
|                 |  日志分析    | 可查看热门文件、热门客户端、热门引用、状态码等维度对文件 URL 进行统计分析|   √  | 
|  辅助工具       |  IP 检测工具    | 可通过该功能验证 IP 地址是否属于又拍云 CDN 节点|   √    | 
|                 |  网络诊断工具    | 检测当前网络连接情况及基本信息，方便定位问题|   √   | 


----------


##产品优势

**自助操作，提升效率**

相对传统 CDN 厂商，又拍云 CDN 服务完全实现全自助化配置，客户可自主进行功能的配置（ 域名配置、回源策略、缓存规则等 ），极大提升了工作效率。

 **资源丰富，全网覆盖**

又拍云 CDN 服务节点资源丰富，实现无差异的网络覆盖，全节点全资源提供服务，真正实现全网加速；网络资源实现本地化运营商覆盖，支持带宽、存储、节点的弹性扩展，避免突发访问激增，打造了目前国内覆盖率最高的内容分发网络，让用户随时随地享受云加速。

**节约成本，简化运营**

用户通过又拍云 CDN 的分发加速，免去了自身架设内容分发网络的时间及资源投入，更能获得非常专业的运维保障服务，简化了客户网站的系统维护，更便捷的对全网进行分发。

**分析数据，精细监控**

又拍云针对所有客户，实现全透明化监控，服务质量可通过又拍云管理控制平台一览无余，为客户业务核心导向提供重要依据。

**运营稳定，服务专业**

又拍云 CDN 作为网络加速服务商，拥有丰富的 CDN 运营经验，深刻理解互联网基础架构，并提供了 7*24 小时无间断的运营服务，保证任何时刻都可以为客户解疑答惑。


----------


##应用场景

又拍云全网加速服务完美融合了又拍云对象存储和 CDN 服务，可以针对网页图片、下载安装包、音视频等文件提供数据托管、分发加速及处理于一体的一站式解决方案。业务使用场景如下：

**网页图片加速**

网页及小文件加速服务帮助客户提升网站的用户访问速度和服务可用性，通过将需要访问的静态内容分发到位于网络边缘的各个缓存服务器中，将用户请求自动分配到距离用户最近的服务器上。建议结合又拍云对象存储服务，可以有效提升内容加载速度，轻松搞定网站图片、短视频等内容分发。

**动态内容加速**

又拍云动态内容加速融合在全网加速服务中，可智能判断 PHP、JSP、ASP 等动态资源文件，自动实现动静分离。通过智能路由、内容压缩、协议优化等技术实现动态内容的加速，完美解决电商购物、在线旅游等网站在登陆、提交订单等动态请求访问速度慢的问题，可进一步提高客户业务转化率。

**大文件下载加速**

又拍云全网加速服务针对网络游戏、软件下载类网站及应用等大文件分发提供了一站式解决方案。由于此类网站及应用存在带宽突发并且由于大文件下载会导致源站服务器承受非常大的压力，又拍云丰富的带宽资源并且结合又拍云对象存储服务，可完美解决大文件带宽突发带来的一系列问题。

**视频点播加速**

又拍云全网加速服务融合了视频点播加速和异步音视频处理服务，针对流媒体点播、音视频网站及应用，又拍云可以提供高速、低价的数据传输服务，帮助在线视频网站、在线教育网站等以流媒体为主的企业提供稳定、高质量、低价的视频分发服务，让您的用户在全国任何地方都可以享受到优质的视频体验。

**自定义 SSL 服务**

又拍云自定义 SSL 加速服务可满足电子商务、在线教育、银行保险等网站在 HTTPS 加速方面的需求，并可以完全满足自主化配置。SSL 服务器数字证书可凭借高强度签名算法，结合服务器端的加密协议，完成 Web 访问客户到服务器间的 HTTPS 加密传输，有效防止 Web 传输中的数据劫持，为网站访问者提供真实、有效、安全的网站内容提供方身份信息，确保用户可放心的浏览网站相关内容。


----------


##资源分布

截至 2016 年 10 月，又拍云国内 CDN 节点数达到 150 多个，覆盖 26 个省份，10 多个运营商，带宽总量超过 1.5TB。2015 年底，又拍云 CDN 节点资源已覆盖新加坡、台湾、香港、美国、德国等海外地区，全面支持海外加速，推进全球化布局。


----------

如有疑问请 [联系我们](https://www.upyun.com/contact)


