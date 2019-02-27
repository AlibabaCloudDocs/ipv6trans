# DescribeIPv6TranslatorAclListAttribute {#reference_c13_24y_m2b .reference}

询访问控制策略组的详细信息，包括访问控制策略组中的IP和关联的IPv6转换映射条目的具体信息。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 DescribeIPv6TranslatorAclListAttribute

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|AclId|String|否|访问控制策略组ID。|
|AclEntryComment|String|否|访问控制策略组中的条目的备注信息。|

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|
|AclId|String| 访问控制策略组ID。

 |
|AclId|String| 访问控制策略组名称。

 |
|AclEntries|String| 访问控制策略组列表。

 |

|名称|类型|描述|
|:-|:-|:-|
|AclEntryIP|String|访问控制策略组条目中要添加的IP条目。|
|AclEntryComment|String| 访问控制策略组条目的备注信息。

 |
|RelatedIPv6TranslatorEntries|List| 问控制策略组关联的IPv6转换映射条目信息

 |

|名称|类型|描述|
|:-|:-|:-|
|Ipv6TranslatorId|String|IPv6转换服务的实例ID。|
|Ipv6TranslatorEntryId|String|IPv6转换映射条目ID。|
|AllocateIpv6Addr|List|IPv6转换服务实例分配的IPv6地址。|
|AllocateIpv6Port|Integer|IPv6转换服务分配的IPv6地址使用的端口。|
|BackendIpv4Addr|String|提供IPv6服务的公网IPv4地址。|
|BackendIpv4Port|Integer|提供IPv6服务的公网IPv4地址使用的端口。|
|TransProtocol|String|协议类型。|
|AclType|String| 访问控制类型，取值：

 white | black

 |

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=DescribeIPv6TranslatorAclLists   
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


