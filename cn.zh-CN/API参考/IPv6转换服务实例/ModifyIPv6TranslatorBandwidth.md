# ModifyIPv6TranslatorBandwidth {#doc_api_1029223 .reference}

修改IPv6转换服务实例的带宽。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Vpc&api=ModifyIPv6TranslatorBandwidth)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ModifyIPv6TranslatorBandwidth|要执行的操作。 取值： **ModifyIPv6TranslatorBandwidth**。

 |
|Bandwidth|Integer|是|2|IPv6转换服务实例的带宽峰值（Mbps），取值： 1-200。

 |
|Ipv6TranslatorId|String|是|ipv6trans-bp1858ysxxxxxx|IPv6转换服务的实例ID。

 |
|RegionId|String|是|cn-hangzhou|IPv6转换服务实例的地域。 您可以通过调用**DescribeRegions**接口获取地域ID。

 |
|AutoPay|Boolean|否|false|是否自动支付预付费实例的账单，取值：

 -   **true**：是
-   **false**（默认）：否

 |
|ClientToken|String|否|sha1111|客户端token，用于保证请求的幂等性。 由客户端生成该参数值，要保证在不同请求间唯一，最大不值过64个 ASCII 字符。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|OrderId|String|202304500950739|订单ID。

 |
|RequestId|String|EF8198EE-8FC9-49C2-A22E-xxxx|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=ModifyIPv6TranslatorBandwidth
&RegionId=cn-hangzhou
&Ipv6TranslatorId=ipv6trans-bp1i8ahxut1iedrqqgbco
&Bandwidth=3
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<ModifyIPv6TranslatorBandwidthResponse>
  <OrderId>202304500950739</OrderId>
  <RequestId>EF8198EE-8FC9-49C2-A22E-010D638D79AF</RequestId>
</ModifyIPv6TranslatorBandwidthResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"EF8198EE-8FC9-49C2-A22E-xxxx",
	"OrderId":"202304500950739"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|403|Forbbiden.SubUser|User not authorized to operate on the specified resource as your account is created by another user.|您没有权限操作该资源，请您申请操作权限后再试。|
|403|Forbidden|User not authorized to operate on the specified resource.|您没有权限操作指定资源，请提交工单咨询。|

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

