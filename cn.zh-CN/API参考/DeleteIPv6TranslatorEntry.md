# DeleteIPv6TranslatorEntry {#reference_mjq_xjy_m2b .reference}

删除IPv6转换映射条目。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 DeleteIPv6TranslatorEntry

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|Ipv6TranslatorId|String|否| IPv6转换服务的实例ID。

 |
|Ipv6TranslatorEntryId|Integer|否| IPv6转换服务映射条目ID。

 |

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=DeleteIPv6TranslatorEntry 
&RegionId=cn-hangzhou
&Ipv6TranslatorId=ipv6trans-bp1i8ahxut1iedrqqgbco
&Ipv6TranslatorEntryId=ipv6transentry-bp1gpgeb3umme48ygihhg
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <DeleteIPv6TranslatorEntryResponse>
          <RequestId>1AE05898-06E5-4782-B4D0-6714DD94C4E6</RequestId>
    </DeleteIPv6TranslatorEntryResponse>
    ```

-   JSON格式

    ```
    {
        "RequestId": "1AE05898-06E5-4782-B4D0-6714DD94C4E6", 
    }
    ```


