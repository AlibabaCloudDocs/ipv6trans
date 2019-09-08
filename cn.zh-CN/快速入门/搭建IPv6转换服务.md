# 搭建IPv6转换服务 {#concept_qp3_kn2_n2b .concept}

本教程指引您快速配置一个IPv6转换服务实例，使本地的IPv4服务器可以接收来自IPv6客户端的请求。

## 前提条件 {#section_nkk_5n2_n2b .section}

本地IPv4服务器已经配置了公网IPv4地址。

## 步骤一 创建IPv6转换服务实例 {#section_xkk_c42_n2b .section}

 在配置IPv6转换映射规则前，您需要先创建一个IPv6转换实例。

完成以下操作，创建IPv6转换服务实例：

1.  登录[IPv6转换服务管理控制台](https://ipv6trans.console.aliyun.com/instances/cn-hangzhou)。
2.  单击**创建IPv6转换实例**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/16069/15679301237291_zh-CN.png)

3.  配置实例。

    本教程中的实例配置如下图所示，更多配置详情参见[实例配置说明](../../../../cn.zh-CN/用户指南/创建IPv6转换服务实例.md#table_p4m_2lq_m2b)。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/16069/15679301237292_zh-CN.png)


## 步骤二 添加映射转发条目 {#section_d4c_hr2_n2b .section}

配置转发条目，将通过IPv6协议转发的请求按照配置的规则转发给指定的IPv4地址。

完成以下操作，添加映射转发条目：

1.  登录[IPv6转换服务管理控制台](https://ipv6trans.console.aliyun.com/instances/cn-hangzhou)。
2.  选择实例的所属地域。
3.  找到目标实例，然后单击**更多** \> **添加映射条目**。
4.  配置转发条目。

    本操作中的配置如下，更多详情参见[映射条目配置说明](../../../../cn.zh-CN/用户指南/添加映射条目.md#table_pml_5cd_n2b)。

    -   **后端IPv4地址**： 要通过映射规则提供IPv6访问的服务器的公网IPv4地址。

        本操作输入**32.0.0.0**

    -   **前端IPv6端口**：  用来接收请求并向后端IPv4服务器进行请求转发的IPv6转换实例的端口。

        本操作输入**80**

    -   **后端IPv4端口**：指定的公网IPv4地址的服务器开放用来接收请求的后端端口。

        本操作输入**80**。

    -   **协议类型**： 用来接收请求并向后端IPv4服务器进行请求转发的协议。

        本操作选择**TCP**。

    -   **条目带宽峰值 **： 本操作输入**1Mbps**。

    -   **条目名称**： 本操作输入**条目1**。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/16069/15679301247294_zh-CN.png)


当实例状态变为**正常**时，表示配置生效。您可以单击监控图标查看流入流量、数据包、连接数等信息。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/16069/15679301247295_zh-CN.png)

