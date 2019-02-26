# RemoveIPv6TranslatorAclListEntry {#reference_ihg_3ny_m2b .reference}

删除访问控制策略组中的IP条目。

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作。 取值：

 AddIPv6TranslatorAclListEntry

 |
|RegionId|String|是| IPv6转换服务实例的地域。

 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|AclId|String|是| 要删除的访问控制策略组ID。

 |
|AclEntries|String|是| 访问控制策略组中要添加的IP条目，可以指定IP地址或IP地址段（CIDR block），多个IP地址/地址段之间用逗号隔开。

 比如：\[\{“entry”:”64:ff96::0203:0102”,”comment”\},\{“entry”:”64::/96”,”comment”\}\]

 |

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#createVPCpub}
https://vpc.aliyuncs.com/?Action=AddIPv6TranslatorAclListEntry
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


