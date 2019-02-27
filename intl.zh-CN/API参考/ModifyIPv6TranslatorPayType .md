# ModifyIPv6TranslatorPayType {#reference_jkr_hdy_m2b .reference}

将后付费实例转换为预付费实例。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 ModifyIPv6TranslatorPayType

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|Ipv6TranslatorId|String|是| IPv6转换服务实例的ID。

 |
|PayType|String|是| IPv6转换服务服务实例的付费类型。取值：

 -   PREPAY：预付费

 |
|PricingCycle|String|是| 预付费的计费周期，取值：

 -   Month：按月购买（默认值）
-   Year：按年购买

 |
|Duration|String|是| 购买时长，取值：

 -   如果计费时长为Month，则取值为\[1,9\]。
-   如果计费时长为Year，则取值为\[1,3\]。

 |
|Autopay|Boolean|否| 是否自动支付预付费实例的帐单（自动续费），取值：

 -   false：否（默认值）
-   true：是

 |

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=ModifyIPv6TranslatorPayType 
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


