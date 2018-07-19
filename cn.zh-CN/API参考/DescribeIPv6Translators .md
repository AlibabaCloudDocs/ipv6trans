# DescribeIPv6Translators {#reference_wkz_b3r_m2b .reference}

查询已创建的IPv6转换服务实例列表。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 DescribeIPv6Translators

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|Ipv6TranslatorId|String|否| IPv6转换服务实例的ID。

 |
|Name|String|否| IPv6转换服务实例的名称。

 |
|Status|String|否| IPv6转换服务实例的状态，取值：

 init|provisioning|active|updating|upgrading|deleting|deleted

 |
|BussinessStatus|String|否| IPv6转换实例的付费状态，取值：

-   Normal：实例创建后，默认状态为正常。
-   FinancialLocked：实例已欠费，或被锁定。

 |
|AllocateIpv6Addr|String|否| 为IPv6转换服务实例分配的IPv6地址。

 |
|AllocatedIpv4Addr|String|否| 为IPv6转换服务实例分配的IPv4地址。

 |
|PayType|String|否| 为IPv6转换服务实例分配的IPv4地址。

 |
|PageNumber|Integer|否| 列表的页码，默认值为1。

 |
|PageSize|Integer|否| 分页查询时每页的行数，最大值为50，默认值为10。

 |

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|
|TotalCount|String|列表条条目数。|
|PageNumber|Integer|当前页码。|
|PageSize|String|每页包含多少条目。|
|Ipv6Translators|List|查询到的IPv6转换服务实例列表。|

|名称|类型|描述|
|:-|:-|:-|
|Ipv6TranslatorId|String| IPv6转换服务实例的ID。

 |
|Name|String| IPv6转换服务实例的名称。

 |
|Spec|String| IPv6转换服务实例的规格。

 |
|Status|String| IPv6转换服务实例的状态。

 |
|BusinessStatus|String| IPv6转换服务实例的付费状态。

 |
|AllocateIpv4Addr|String|分配的IPv6转换服务实例的IPv4地址。|
|AllocateIpv6Addr|String|分配的IPv6转换服务实例的IPv6地址。|
|PayType|String|IPv6转换服务实例的付费类型。|
|CreateTime|String|IPv6转换服务实例的创建时间。|
|EndTime|Boolean|IPv6转换服务实例的到期时间。|
|Bandwidth|Integer|IPv6转换服务实例的带宽。|
|AvailableBandwidth|Integer|IPv6转换服务实例可用的带宽。|
|Ipv6TranslatorEntryIds|List|IPv6转换服务实例的转换映射条目ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=DescribeVpcs
&RegionId=us-west-1
&CidrBlock=10.10.0.0/24
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


