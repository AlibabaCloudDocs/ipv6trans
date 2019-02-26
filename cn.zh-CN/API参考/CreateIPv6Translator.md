# CreateIPv6Translator {#reference_ull_qdr_m2b .reference}

创建IPv6转换服务实例。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 CreateIPv6Translator

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|Spec|String|否| IPv6转换服务服务实例的规格。取值：

 -   small

 |
|Name|String|否| IPv6转换服务实例的名称，默认为实例ID。

 长度为 2-100个字符，必须以字母或中文开头，可包含数字，点号（.），下划线（\_）和短横线（-）。但不能以`http://` 或`https://`开头。

 |
|PayType|String|否| IPv6转换服务服务实例的付费类型。取值：

 -   PREPAY：预付费
-   POSTPAY：后付费

 |
|PricingCycle|String|否| 预付费的计费周期，取值：

 -   Month：按月购买（默认值）
-   Year：按年购买

 |
|Duration|String|否| 购买时长，取值：

 -   如果计费时长为Month，则取值为\[1,9\]。
-   如果计费时长为Year，则取值为\[1,3\]。

 |
|Autopay|Boolean|否| 是否自动支付预付费实例的帐单，取值：

 -   false：否（默认值）
-   true：是

 |
|Bandwidth|Integer|否| IPv6转换服务实例的计费带宽（Mbps）。取值：

 \[1,200\]

 若不设置转换映射条目的带宽，实例中的IPv6转换服务映射条目共享该带宽。

**说明：** 若不指定带宽，默认值为10Mbps。

 |
|ClientToken|String|否|客户端token用于保证请求的幂等性。要保证Client Token在不同请求间唯一，最大值不超过64个ASCII字符。|

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|
|Ipv6TranslatorId|String|IPv6转换服务实例ID。|
|Name|String|IPv6转换服务实例名称。|
|Spec|String|IPv6转换服务实例规格。|
|OrderId|String|创建IPv6转换服务实例的订单ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=CreateIPv6Translator
&RegionId=cn-hangzhou
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8" ?>
    <CreateIPv6TranslatorResponse>
    	<Ipv6TranslatorId>ipv6trans-bp1i8ahxut1iedrqqgbco</Ipv6TranslatorId>
    	<Name>test_nat64gw_autopay_0725</Name>
    	<OrderId>202303300940739</OrderId>
    	<RequestId>1AE05898-06E5-4782-B4D0-6714DD94C4E6</RequestId>
    	<Spec>small</Spec>
    </CreateIPv6TranslatorResponse>
    ```

-   JSON格式

    ```
    {
        "Ipv6TranslatorId": "ipv6trans-bp1i8ahxut1iedrqqgbco", 
        "Name": "test_nat64gw_autopay_0725", 
        "OrderId": 202303300940739, 
        "RequestId": "1AE05898-06E5-4782-B4D0-6714DD94C4E6", 
        "Spec": "small"
    }
    ```


