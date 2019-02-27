# DescribeIPv6Translators {#doc_api_1027218 .reference}

查询已创建的IPv6转换服务实例列表。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Vpc&api=DescribeIPv6Translators)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeIPv6Translators|要执行的操作。 取值： **DescribeIPv6Translators**。

 |
|RegionId|String|是|cn-hangzhou|IPv6转换服务实例的地域。 您可以通过调用**DescribeRegions**接口获取地域ID。

 |
|AllocateIpv4Addr|String|否|47.99.xx.xx,47.99.xx.xx|为IPv6转换服务实例分配的IPv4地址。

 |
|AllocateIpv6Addr|String|否|2400:3200:1600::xxx|为IPv6转换服务实例分配的IPv6地址。

 |
|BusinessStatus|String|否|Normal|IPv6转换服务实例的业务状态。

 |
|Ipv6TranslatorId|String|否|ipv6trans-bp1858ysxxxxxx|IPv6转换服务实例的ID。

 |
|Name|String|否|ipv6\_1|IPv6转换服务实例的名称。

 |
|PageNumber|Integer|否|1|列表的页码，默认值为1。

 |
|PageSize|Integer|否|1|分页查询时每页的行数，最大值为50，默认值为10。

 |
|PayType|String|否|Prepay|为IPv6转换服务实例分配的IPv4地址。

 |
|Spec|String|否|small|IPv6转换服务实例的规格。

 |
|Status|String|否|active|IPv6转换服务实例的状态，取值：**init|provisioning|active|updating|upgrading|deleting|deleted**。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Ipv6Translators| | |查询到的IPv6转换服务实例列表。

 |
|└AllocateIpv4Addr|String|47.99.xx.xx,47.99.xx.xx|分配的IPv6转换服务实例的IPv4地址。

 |
|└AllocateIpv6Addr|String|2400:3200:1600::xxx|分配的IPv6转换服务实例的IPv6地址。

 |
|└AvailableBandwidth|String|1|IPv6转换服务实例可用的带宽。

 |
|└Bandwidth|Integer|1|IPv6转换服务实例的带宽。

 |
|└BusinessStatus|String|Normal|IPv6转换服务实例的付费状态。

 |
|└CreateTime|Long|1537151540000|IPv6转换服务实例的创建时间。

 |
|└Description|String|descriptionforinstance|IPv6转换服务实例的描述。

 |
|└EndTime|Long|1539792000000|IPv6转换服务实例的到期时间。

 |
|└Ipv6TranslatorEntryIds| |\["ipv6transentry-bp1kp5ixtm3001vmnfzpw", "ipv6transentry-bp16dg87v006zwrd6qd78" \]|IPv6转换服务实例的转换映射条目ID。

 |
|└Ipv6TranslatorId|String|ipv6trans-bp1858ysxxxxxx|IPv6转换服务实例的ID。

 |
|└Name|String|test|IPv6转换服务实例的名称。

 |
|└PayType|String|Prepay|IPv6转换服务实例的付费类型。

 |
|└Spec|String|small|IPv6转换服务实例的规格。

 |
|└Status|String|active|IPv6转换服务实例的状态。

 |
|PageNumber|Integer|1|当前页码。

 |
|PageSize|Integer|10|每页包含多少条目。

 |
|RequestId|String|3109D437-5D6D-4A28-B5F5-EF936DExxxx|请求ID。

 |
|TotalCount|Integer|1|列表条条目数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=DescribeIPv6Translators
&RegionId=us-west-1
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeIPv6TranslatorsResponse>
  <PageNumber>1</PageNumber>
  <TotalCount>1</TotalCount>
  <PageSize>10</PageSize>
  <RequestId>3109D437-5D6D-4A28-B5F5-EF936DExxxx</RequestId>
  <Ipv6Translators>
    <Ipv6Translator>
      <Spec>small</Spec>
      <Ipv6TranslatorId>ipv6trans-bp1858ysxxxxxx</Ipv6TranslatorId>
      <AllocateIpv6Addr>2400:3200:1600::xxx</AllocateIpv6Addr>
      <Name>test</Name>
      <Status>active</Status>
      <Ipv6TranslatorEntryIds>
        <Ipv6TranslatorEntryId>ipv6transentry-bp1g8bhrdexxxxx</Ipv6TranslatorEntryId>
      </Ipv6TranslatorEntryIds>
      <AllocateIpv4Addr>47.99.xx.xx,47.99.xx.xx</AllocateIpv4Addr>
      <BusinessStatus>Normal</BusinessStatus>
      <CreateTime>1537151540000</CreateTime>
      <RegionId>cn-hangzhou</RegionId>
      <EndTime>1539792000000</EndTime>
      <AvailableBandwidth>1</AvailableBandwidth>
      <PayType>Prepay</PayType>
      <Bandwidth>1</Bandwidth>
    </Ipv6Translator>
  </Ipv6Translators>
</DescribeIPv6TranslatorsResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"PageNumber":1,
	"TotalCount":1,
	"PageSize":10,
	"RequestId":"3109D437-5D6D-4A28-B5F5-EF936DExxxx",
	"Ipv6Translators":{
		"Ipv6Translator":[
			{
				"Spec":"small",
				"Ipv6TranslatorId":"ipv6trans-bp1858ysxxxxxx",
				"AllocateIpv6Addr":"2400:3200:1600::xxx",
				"Name":"test",
				"Status":"active",
				"Ipv6TranslatorEntryIds":{
					"Ipv6TranslatorEntryId":[
						"ipv6transentry-bp1g8bhrdexxxxx"
					]
				},
				"AllocateIpv4Addr":"47.99.xx.xx,47.99.xx.xx",
				"BusinessStatus":"Normal",
				"CreateTime":1537151540000,
				"RegionId":"cn-hangzhou",
				"EndTime":1539792000000,
				"AvailableBandwidth":1,
				"PayType":"Prepay",
				"Bandwidth":1
			}
		]
	}
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|403|Forbbiden.SubUser|User not authorized to operate on the specified resource as your account is created by another user.|您没有权限操作该资源，请您申请操作权限后再试。|
|403|Forbidden|User not authorized to operate on the specified resource.|您没有权限操作指定资源，请提交工单咨询。|

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

