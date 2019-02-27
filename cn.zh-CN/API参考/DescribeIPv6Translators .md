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
https://vpc.aliyuncs.com/?Action=DescribeIPv6Translators
&RegionId=us-west-1
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8" ?>
    <DescribeIPv6TranslatorsResponse>
    	<TotalCount>4</TotalCount>
    	<PageSize>10</PageSize>
    	<RequestId>FCA1654C-98D4-431B-8BCA-E7A58403E3F5</RequestId>
    	<PageNumber>1</PageNumber>
    	<Ipv6Translators>
    		<Ipv6Translator>
    			<Status>active</Status>
    			<Description>haha1</Description>
    			<EndTime>1534780800000</EndTime>
    			<AvailableBandwidth>9</AvailableBandwidth>
    			<Ipv6TranslatorEntryIds>
    				<Ipv6TranslatorEntryId>ipv6transentry-bp1kp5ixtm3001vmnfzpw</Ipv6TranslatorEntryId>
    				<Ipv6TranslatorEntryId>ipv6transentry-bp16dg87v006zwrd6qd78</Ipv6TranslatorEntryId>
    			</Ipv6TranslatorEntryIds>
    			<CreateTime>1532067890000</CreateTime>
    			<Ipv6TranslatorId>ipv6trans-bp1bfkv90v1a3h14y8900</Ipv6TranslatorId>
    			<PayType>Prepay</PayType>
    			<BusinessStatus>Normal</BusinessStatus>
    			<Name>nat64_test_news</Name>
    			<AllocateIpv6Addr>2400:3200:1600::97</AllocateIpv6Addr>
    			<AllocateIpv4Addr>47.99.56.116,47.99.58.215</AllocateIpv4Addr>
    			<Bandwidth>11</Bandwidth>
    			<RegionId>cn-hangzhou</RegionId>
    			<Spec>small</Spec>
    		</Ipv6Translator>
    		<Ipv6Translator>
    			<Status>active</Status>
    			<EndTime>1535126400000</EndTime>
    			<AvailableBandwidth>1</AvailableBandwidth>
    			<Ipv6TranslatorEntryIds></Ipv6TranslatorEntryIds>
    			<CreateTime>1532422850000</CreateTime>
    			<Ipv6TranslatorId>ipv6trans-bp1tkg5he8yg8dc872ut3</Ipv6TranslatorId>
    			<PayType>Prepay</PayType>
    			<BusinessStatus>Normal</BusinessStatus>
    			<Name>a</Name>
    			<AllocateIpv6Addr>2400:3200:1600::202</AllocateIpv6Addr>
    			<AllocateIpv4Addr>47.97.117.218,116.62.230.28</AllocateIpv4Addr>
    			<Bandwidth>1</Bandwidth>
    			<RegionId>cn-hangzhou</RegionId>
    			<Spec>small</Spec>
    		</Ipv6Translator>
    		<Ipv6Translator>
    			<Status>active</Status>
    			<EndTime>1533916800000</EndTime>
    			<AvailableBandwidth>1</AvailableBandwidth>
    			<Ipv6TranslatorEntryIds>
    				<Ipv6TranslatorEntryId>ipv6transentry-bp1ibs9smg9xl92vm73ou</Ipv6TranslatorEntryId>
    				<Ipv6TranslatorEntryId>ipv6transentry-bp1v27z2lu1dm92fefxbn</Ipv6TranslatorEntryId>
    			</Ipv6TranslatorEntryIds>
    			<CreateTime>1531208465000</CreateTime>
    			<Ipv6TranslatorId>ipv6trans-bp1k41ey4z25dstw69w19</Ipv6TranslatorId>
    			<PayType>Prepay</PayType>
    			<BusinessStatus>Normal</BusinessStatus>
    			<Name>test_0710_image33test_0710_image33test_0710_image33test_0710_image33test_0710_image33</Name>
    			<AllocateIpv6Addr>2400:3200:1600::145</AllocateIpv6Addr>
    			<AllocateIpv4Addr>47.99.41.204,47.99.34.154</AllocateIpv4Addr>
    			<Bandwidth>1</Bandwidth>
    			<RegionId>cn-hangzhou</RegionId>
    			<Spec>small</Spec>
    		</Ipv6Translator>
    		<Ipv6Translator>
    			<Status>active</Status>
    			<EndTime>1534003200000</EndTime>
    			<AvailableBandwidth>1</AvailableBandwidth>
    			<Ipv6TranslatorEntryIds></Ipv6TranslatorEntryIds>
    			<CreateTime>1531273620000</CreateTime>
    			<Ipv6TranslatorId>ipv6trans-bp1s7u98sqx0j3319jibk</Ipv6TranslatorId>
    			<PayType>Prepay</PayType>
    			<BusinessStatus>Normal</BusinessStatus>
    			<Name>test_0711_02</Name>
    			<AllocateIpv6Addr>2400:3200:1600::91</AllocateIpv6Addr>
    			<AllocateIpv4Addr>47.97.165.31,47.99.40.132</AllocateIpv4Addr>
    			<Bandwidth>1</Bandwidth>
    			<RegionId>cn-hangzhou</RegionId>
    			<Spec>small</Spec>
    		</Ipv6Translator>
    	</Ipv6Translators>
    </DescribeIPv6TranslatorsResponse>
    ```

-   JSON格式

    ```
    {
        "TotalCount": 4, 
        "PageSize": 10, 
        "RequestId": "FCA1654C-98D4-431B-8BCA-E7A58403E3F5", 
        "PageNumber": 1, 
        "Ipv6Translators": {
            "Ipv6Translator": [
                {
                    "Status": "active", 
                    "Description": "haha1", 
                    "EndTime": 1534780800000, 
                    "AvailableBandwidth": 9, 
                    "Ipv6TranslatorEntryIds": {
                        "Ipv6TranslatorEntryId": [
                            "ipv6transentry-bp1kp5ixtm3001vmnfzpw", 
                            "ipv6transentry-bp16dg87v006zwrd6qd78"
                        ]
                    }, 
                    "CreateTime": 1532067890000, 
                    "Ipv6TranslatorId": "ipv6trans-bp1bfkv90v1a3h14y8900", 
                    "PayType": "Prepay", 
                    "BusinessStatus": "Normal", 
                    "Name": "nat64_test_news", 
                    "AllocateIpv6Addr": "2400:3200:1600::97", 
                    "AllocateIpv4Addr": "47.99.56.116,47.99.58.215", 
                    "Bandwidth": 11, 
                    "RegionId": "cn-hangzhou", 
                    "Spec": "small"
                }, 
                {
                    "Status": "active", 
                    "EndTime": 1535126400000, 
                    "AvailableBandwidth": 1, 
                    "Ipv6TranslatorEntryIds": {
                        "Ipv6TranslatorEntryId": [ ]
                    }, 
                    "CreateTime": 1532422850000, 
                    "Ipv6TranslatorId": "ipv6trans-bp1tkg5he8yg8dc872ut3", 
                    "PayType": "Prepay", 
                    "BusinessStatus": "Normal", 
                    "Name": "a", 
                    "AllocateIpv6Addr": "2400:3200:1600::202", 
                    "AllocateIpv4Addr": "47.97.117.218,116.62.230.28", 
                    "Bandwidth": 1, 
                    "RegionId": "cn-hangzhou", 
                    "Spec": "small"
                }, 
                {
                    "Status": "active", 
                    "EndTime": 1533916800000, 
                    "AvailableBandwidth": 1, 
                    "Ipv6TranslatorEntryIds": {
                        "Ipv6TranslatorEntryId": [
                            "ipv6transentry-bp1ibs9smg9xl92vm73ou", 
                            "ipv6transentry-bp1v27z2lu1dm92fefxbn"
                        ]
                    }, 
                    "CreateTime": 1531208465000, 
                    "Ipv6TranslatorId": "ipv6trans-bp1k41ey4z25dstw69w19", 
                    "PayType": "Prepay", 
                    "BusinessStatus": "Normal", 
                    "Name": "test_0710_image33test_0710_image33test_0710_image33test_0710_image33test_0710_image33", 
                    "AllocateIpv6Addr": "2400:3200:1600::145", 
                    "AllocateIpv4Addr": "47.99.41.204,47.99.34.154", 
                    "Bandwidth": 1, 
                    "RegionId": "cn-hangzhou", 
                    "Spec": "small"
                }, 
                {
                    "Status": "active", 
                    "EndTime": 1534003200000, 
                    "AvailableBandwidth": 1, 
                    "Ipv6TranslatorEntryIds": {
                        "Ipv6TranslatorEntryId": [ ]
                    }, 
                    "CreateTime": 1531273620000, 
                    "Ipv6TranslatorId": "ipv6trans-bp1s7u98sqx0j3319jibk", 
                    "PayType": "Prepay", 
                    "BusinessStatus": "Normal", 
                    "Name": "test_0711_02", 
                    "AllocateIpv6Addr": "2400:3200:1600::91", 
                    "AllocateIpv4Addr": "47.97.165.31,47.99.40.132", 
                    "Bandwidth": 1, 
                    "RegionId": "cn-hangzhou", 
                    "Spec": "small"
                }
            ]
        }
    }
    ```


