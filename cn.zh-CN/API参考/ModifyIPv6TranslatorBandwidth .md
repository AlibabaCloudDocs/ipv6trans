# ModifyIPv6TranslatorBandwidth {#reference_oqq_rcy_m2b .reference}

修改IPv6转换服务实例的带宽。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 ModifyIPv6TranslatorPayType

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|Ipv6TranslatorId|String|是| IPv6转换服务的实例ID。

 |
|Bandwidth|String|是| IPv6转换服务实例的带宽峰值（Mbps），取值：

 \[1,200\]

 |
|AutoPay|Boolean|是| 是否自动支付预付费实例的账单，取值：

 -   true：是
-   false（默认）：否

 |

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|
|OrderId|String|订单ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=ModifyIPv6TranslatorPayType
&RegionId=cn-hangzhou
&Ipv6TranslatorId=ipv6trans-bp1i8ahxut1iedrqqgbco
&Bandwidth=3
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <ModifyIPv6TranslatorPayTypeResponse>
    	<OrderId>202304500950739</OrderId>
    	<RequestId>EF8198EE-8FC9-49C2-A22E-010D638D79AF</RequestId>
    </ModifyIPv6TranslatorPayTypeResponse>
    ```

-   JSON格式

    ```
    {
        "OrderId": "202304500950739", 
        "RequestId": "EF8198EE-8FC9-49C2-A22E-010D638D79AF"
    }
    ```


