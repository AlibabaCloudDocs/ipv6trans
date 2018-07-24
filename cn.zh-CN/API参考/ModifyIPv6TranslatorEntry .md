# ModifyIPv6TranslatorEntry {#reference_uqw_1jy_m2b .reference}

修改IPv6转换映射条目。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 ModifyIPv6TranslatorEntry

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|Ipv6TranslatorId|String|是| IPv6转换服务的实例ID。

 |
|AllocateIpv6Port|Integer|否| IPv6转换服务实例分配的IPv6地址的使用端口。

 |
|BackendIpv4Addr|String|否| 需要提供IPv6服务的公网IPv4地址（IPv4-only的服务器的IPv4地址）。

 |
|BackendIpv4Port|Integer|否|需要提供IPv6服务的公网IPv4地址的端口。|
|TransProtocol|String|否| 协议类型。取值：

 -   tcp：转发TCP协议的报文。
-   udp：转发UDP协议的报文。

 |
|EntryBandwidth|Integer|否| IPv6转换映射条目的带宽峰值。取值：

-   -1（默认值）：不限制IPv6转换映射条目的带宽峰值。
-   1-200Mbps：改映射条目的带宽值。

**说明：** 所有IPv6转换映射条目的带宽峰值之和不能超过实例的带宽峰值。


 |
|EntryName|String|否| IPv6转换映射条目的名称。

 长度为 2-100个字符，必须以字母或中文开头，可包含数字，点号（.），下划线（\_）和短横线（-）。但不能以`http://` 或`https://`开头。

 |
|EntryDescription|String|否| IPv6转换映射条目的描述信息。

 长度为 2-100个字符，必须以字母或中文开头，可包含数字，点号（.），下划线（\_）和短横线（-）。但不能以`http://` 或`https://`开头。

 |

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|
|Ipv6TranslatorEntryId|String|IPv6转换服务映射条目ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=ModifyIPv6TranslatorEntry 
&RegionId=cn-hangzhou
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <CreateVpcResponse>
    </CreateVpcResponse>
    ```

-   JSON格式

    ```
    
    
    ```


