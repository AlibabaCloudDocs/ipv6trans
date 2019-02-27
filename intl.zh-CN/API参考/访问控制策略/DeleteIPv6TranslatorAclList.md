# DeleteIPv6TranslatorAclList {#doc_api_1026717 .reference}

删除访问控制策略组。只有当访问控制策略组没有绑定任何IPv6转换映射时，才可以删除。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Vpc&api=DeleteIPv6TranslatorAclList)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteIPv6TranslatorAclList|要执行的操作。 取值： DeleteIPv6TranslatorAclList

 |
|RegionId|String|是|cn-hangzhou|IPv6转换服务实例的地域。 您可以通过调用 DescribeRegions接口获取地域ID。

 |
|AclId|String|否|ipv6transacl-bp1de2xxxx|要删除的访问控制策略组ID。

 |
|ClientToken|String|否|sha123456|客户端token，用于保证请求的幂等性。 由客户端生成该参数值，要保证在不同请求间唯一，最大不值过64个 ASCII 字符。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|8B2F5262-6B57-43F2-xxxxx|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=DeleteIPv6TranslatorAclList
&RegionId=cn-hangzhou
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteIPv6TranslatorAclListResponse>
  <RequestId>0ED8D006-F706-4D23-88ED-E11ED28DCAC0</RequestId>
</DeleteIPv6TranslatorAclListResponse>

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

