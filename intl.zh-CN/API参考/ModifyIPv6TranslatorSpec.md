# ModifyIPv6TranslatorSpec {#reference_lx1_3zx_m2b .reference}

修改IPv6转换服务实例的规格。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 ModifyIPv6TranslatorAttribute

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|Ipv6TranslatorId|String|是| IPv6转换服务实例的ID。

 |
|Spec|String|是| IPv6转换服务服务实例的规格。取值：

 -   small

 |

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=ModifyIPv6TranslatorSpec
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


