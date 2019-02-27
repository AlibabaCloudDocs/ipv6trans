# DeleteIPv6TranslatorEntry {#doc_api_1029468 .reference}

删除IPv6转换映射条目。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Vpc&api=DeleteIPv6TranslatorEntry)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteIPv6TranslatorEntry|要执行的操作。 取值： **DeleteIPv6TranslatorEntry**。

 |
|RegionId|String|是|cn-hangzhou|IPv6转换服务实例的地域。 您可以通过调用**DescribeRegions**接口获取地域ID。

 |
|ClientToken|String|否|sha11112222|客户端token，用于保证请求的幂等性。 由客户端生成该参数值，要保证在不同请求间唯一，最大不值过64个 ASCII 字符。

 |
|Ipv6TranslatorEntryId|String|否|ipv6transentry-bp1g8bhrdexxxxx|要删除的IPv6转换服务映射条目ID。

 |
|Ipv6TranslatorId|String|否|ipv6trans-bp1858ysxxxxxx|IPv6转换服务的实例ID。

 **说明：** 如果您不指定**Ipv6TranslatorEntryId**参数，则删除指定实例下所有的映射条目。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|8B2F5262-6B57-43F2-xxxxx|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=DeleteIPv6TranslatorEntry
&RegionId=cn-hangzhou
&Ipv6TranslatorId=ipv6trans-bp1i8ahxutxxx
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteIPv6TranslatorEntryResponse>
  <RequestId>1AE05898-06E5-4782-B4D0-6714DD94C4E6</RequestId>
</DeleteIPv6TranslatorEntryResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"8B2F5262-6B57-43F2-xxxxx"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|403|Forbbiden.SubUser|User not authorized to operate on the specified resource as your account is created by another user.|您没有权限操作该资源，请您申请操作权限后再试。|
|403|Forbidden|User not authorized to operate on the specified resource.|您没有权限操作指定资源，请提交工单咨询。|

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

