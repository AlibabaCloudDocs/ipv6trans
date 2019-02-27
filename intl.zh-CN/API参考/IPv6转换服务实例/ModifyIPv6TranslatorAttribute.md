# ModifyIPv6TranslatorAttribute {#doc_api_1027219 .reference}

修改IPv6转换服务实例的名称和描述信息。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Vpc&api=ModifyIPv6TranslatorAttribute)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyIPv6TranslatorAttribute|要执行的操作。 取值： **ModifyIPv6TranslatorAttribute**。

 |
|Ipv6TranslatorId|String|是|ipv6trans-bp1858ysxxxxxx|IPv6转换服务实例的ID。

 |
|RegionId|String|是|cn-hangzhou|IPv6转换服务实例的地域。 您可以通过调用**DescribeRegions**接口获取地域ID。

 |
|ClientToken|String|否|sha1111|客户端token用于保证请求的幂等性。要保证Client Token在不同请求间唯一，最大值不超过64个ASCII字符。

 |
|Description|String|否|instancedescription|IPv6转换服务的描述信息。默认值为空。 长度为 2-100个字符，必须以字母或中文开头，可包含数字，点号（.），下划线（\_）和短横线（-）。但不能以http:// 或https://开头。

 |
|Name|String|否|instancename|IPv6转换服务实例的名称，默认为实例ID。 长度为 2-100个字符，必须以字母或中文开头，可包含数字，点号（.），下划线（\_）和短横线（-）。但不能以http:// 或https://开头。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|8B2F5262-6B57-43F2-xxxxx|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=ModifyIPv6TranslatorAttribute
&RegionId=cn-hangzhou
&Ipv6TranslatorId=ipv6trans-bp1i8xxxxx
&Name=test
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifyIPv6TranslatorAttributeResponse>
  <RequestId>AD006AF1-E5F8-49D3-82E2-3333F27103FF</RequestId>
</ModifyIPv6TranslatorAttributeResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"AD006AF1-E5F8-49D3-82E2-3333F27103FF"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|403|Forbbiden.SubUser|User not authorized to operate on the specified resource as your account is created by another user.|您没有权限操作该资源，请您申请操作权限后再试。|
|403|Forbidden|User not authorized to operate on the specified resource.|您没有权限操作指定资源，请提交工单咨询。|

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

