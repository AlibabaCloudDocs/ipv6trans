# DescribeIPv6TranslatorEntries {#reference_p41_fgy_m2b .reference}

查询IPv6转换映射条目。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 DescribeIPv6TranslatorEntries

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|Ipv6TranslatorId|String|是| IPv6转换服务实例的ID。

**说明：** 如果值为null，查询全部映射条目。

 |
|Ipv6TranslatorEntryId|String|否| 要查询的IPv6转换映射条目ID。

**说明：** 

-   如果Ipv6TranslatorId参数和Ipv6TranslatorEntryId参数的值都为null，则返回所有IPv6转换映射条目信息。
-   如果仅是Ipv6TranslatorEntryId参数的值为null，则返回当前IPv6转换服务实例下的所有IPv6转换映射条目信息。

 |
|AllocateIpv6Addr|String|否|IPv6转换服务实例分配的IPv6地址。|
|AllocateIpv6Port|Integer|否| IPv6转换服务实例分配的IPv6地址使用的端口。

 |
|BackendIpv4Addr|String|否| 需要提供IPv6服务的公网IPv4地址

 |
|BackendIpv4Port|Integer|否| 需要提供IPv6服务的公网IPv4地址使用的端口。

 |
|TransProtocol|String|否| 转发数据的协议类型。

 |
|EntryName|String|否| Pv6转换映射条目的名称。

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
|Ipv6TranslatorEntries|List|查询到的IPv6转换映射条目。|

|名称|类型|描述|
|:-|:-|:-|
|Ipv6TranslatorEntryId|String| IPv6转换映射条目ID。

 |
|Ipv6TranslatorId|String| IPv6转换映射条目所属的IPv6转换服务实例ID。

 |
|RegionId|String| IPv6转换服务实例的地域。

 |
|AllocateIpv6Port|Integer| IPv6转换服务实例分配的IPv6地址的使用端口。

 |
|BackendIpv4Port|String|提供IPv6服务的IPv4公网地址。|
|AllocateIpv6Addr|String|分配的IPv6转换服务实例的IPv6地址。|
|TransProtocol|String|协议类型。|
|EntryBandwidth|String|IPv6转换映射条目的带宽。|
|EntryStatus|Boolean|IPv6转换映射条目的状态。|
|EntryName|Integer|IPv6转换映射条目的名称。|
|EntryDescription|Integer|IPv6转换映射条目的描述。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=DescribeIPv6TranslatorEntries
&RegionId=cn-hangzhou
&Ipv6TranslatorId=ipv6transentry-bp1gpgeb3umme48ygihhg
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8" ?>
    <DescribeIPv6TranslatorEntriesResponse>
    	<Ipv6TranslatorEntries>
    		<AllocateIpv6Addr>2400:3200:1600::224</AllocateIpv6Addr>
    		<AllocateIpv6Port>2345</AllocateIpv6Port>
    		<BackendIpv4Addr>222.118.1.3</BackendIpv4Addr>
    		<BackendIpv4Port>1234</BackendIpv4Port>
    		<EntryBandwidth>-1</EntryBandwidth>
    		<EntryStatus>active</EntryStatus>
    		<Ipv6TranslatorEntryId>ipv6transentry-bp1gpgeb3umme48ygihhg</Ipv6TranslatorEntryId>
    		<Ipv6TranslatorId>ipv6trans-bp1i8ahxut1iedrqqgbco</Ipv6TranslatorId>
    		<RegionId>cn-hangzhou</RegionId>
    		<TransProtocol>tcp</TransProtocol>
    	</Ipv6TranslatorEntries>
    	<PageNumber>1</PageNumber>
    	<PageSize>10</PageSize>
    	<RequestId>9C57C407-3179-4B85-80D8-F0BE74262EF1</RequestId>
    	<TotalCount>1</TotalCount>
    </DescribeIPv6TranslatorEntriesResponse>
    ```

-   JSON格式

    ```
    {
        "Ipv6TranslatorEntries": [
            {
                "AllocateIpv6Addr": "2400:3200:1600::224", 
                "AllocateIpv6Port": 2345, 
                "BackendIpv4Addr": "222.118.1.3", 
                "BackendIpv4Port": "1234", 
                "EntryBandwidth": "-1", 
                "EntryStatus": "active", 
                "Ipv6TranslatorEntryId": "ipv6transentry-bp1gpgeb3umme48ygihhg", 
                "Ipv6TranslatorId": "ipv6trans-bp1i8ahxut1iedrqqgbco", 
                "RegionId": "cn-hangzhou", 
                "TransProtocol": "tcp"
            }
        ], 
        "PageNumber": 1, 
        "PageSize": 10, 
        "RequestId": "9C57C407-3179-4B85-80D8-F0BE74262EF1", 
        "TotalCount": 1
    }
    ```


