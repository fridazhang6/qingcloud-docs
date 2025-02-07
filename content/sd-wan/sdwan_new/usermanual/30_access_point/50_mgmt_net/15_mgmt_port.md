---
title: "配置端口分流"
draft: false
collapsible: false
weight: 15

---

配置端口分流可决定网口数据走互联网流量还是隧道流量，若当前网口数据负载过高，也可配置端口分流，将当前网口数据流量分配到其它 WAN 口或业务组减少当前网口的负载。

本章节介绍如何配置端口分流。

## 前提条件

- 已获取 QingCloud 管理控制台账号和密码。
- 已创建连接云网。
- 已创建接入点。

## 操作步骤

### 添加分流路由

1. 登录 QingCloud 管理控制台。

2. 选择**产品与服务** > **SD-WAN（新版）** > **SD-WAN（新版）**，进入**连接云网**页面。

   <img src="../../../../_images/qs_cloud_network.png" style="zoom:50%;" />

3. 在左侧导航栏中，点击**接入点**，进入**接入点**页面。

   <img src="../../../../_images/qs_light_access.png" style="zoom:50%;" />

4. 点击接入点名称，进入接入点详情页面。

5. 选择**网络管理** > **端口分流**，进入**端口分流**页面。

   <img src="../../../../_images/port_f01.png" style="zoom:100%;" />

6. 点击**添加分流路由**，弹出**添加分流路由**窗口。

7. 根据提示信息输入参数信息。

   | 参数     | 参数说明                                                     |
   | -------- | ------------------------------------------------------------ |
   | 名称     | 设置分流路由的名称。                                         |
   | 源类型   | 源 IP 地址类型，当前仅支持 IP地址                            |
   | 源 IP    | 可输入IP地址、IP段和IP地址范围，请使用换行符进行分隔，0.0.0.0/0代表不限制IP。 |
   | 目的类型 | 目的 IP 地址类型，目前仅支持 IP地址                          |
   | 目的 IP  | 可输入IP地址、IP段和IP地址范围，请使用换行符进行分隔，0.0.0.0/0代表不限制IP。 |
   | WAN 端口 | 可选择默认业务组或[自定义业务组](/sd-wan/sdwan_new/usermanual/30_access_point/40_mgmt_equipment/20_config_wan/#相关操作)。 |

8. 点击**添加**，完成分流路由的添加操作。

9. 点击**应用修改**，使配置生效。

   添加静态路由后默认为**启用**状态。

## 相关操作

### 禁用分流路由

1. 进入**网络管理** > **端口分流**页面。

2. 在已添加的分流路由所在行的**操作**列中，点击**禁用**。

   若页面分流路由的状态变成为**禁用**，则说明禁用成功。

3. 点击**应用修改**，使配置生效。

### 修改分流路由

1. 进入**网络管理** > **端口分流**页面。

2. 在已添加的分流路由所在行的**操作**列中，点击**修改**，弹出**修改分流路由**窗口。

3. 修改完成后，点击**应用修改**，完成分流路由的修改。

   若页面弹出**编辑成功**提示信息，则说明修改分流路由成功。

4. 点击**应用修改**，使配置生效。

### 删除修改路由

1. 进入**网络管理** > **端口分流**页面。

2. 在已添加的分流路由所在行的**操作**列中，点击**删除**，弹出提示窗口。

3. 点击**确定**，完成分流路由删除操作。

   若页面弹出**删除成功**提示信息，则说明删除分流路由成功。

4. 点击**应用修改**，使删除生效。