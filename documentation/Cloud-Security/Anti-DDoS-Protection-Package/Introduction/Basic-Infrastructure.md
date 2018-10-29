# 基础架构

DDoS防护包是一款针对京东云内业务，快速提升其抗D防护能力的增值服务。

用户购买防护包后，立即获得套餐对应的DDoS防护能力，无需复杂配置或更换公网IP地址。目前支持京东云内的云主机、负载均衡、容器、Web应用服务器等服务抗D能力提升。

## 产品架构
京东云DDoS防护包作为DDoS基础防护的升级版，其架构图和基础防护一致，但是会提供更大的DDoS防护能力。

![防护包架构图](https://github.com/jdclouddocs/cn/blob/anti-ddos/image/Anti-DDoS-Protection-Package/防护包架构图.png)

如图所示，在京东云机房出口处，旁路部署DDoS攻击检测及清洗设备。实时对Internet的网络流量进行检测，一旦发现流量异常，就将所有流量自动牵引到清洗设备，完成一系列流量清洗后，干净的流量再回源到用户服务器。