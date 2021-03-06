# CreateIPv6TranslatorEntry {#doc_api_1027239 .reference}

为指定的IPv6转换服务实例添加IPv6转换映射条目。

## 调试 {#apiExplorer .section}

前往【[API Explorer](https://api.aliyun.com/#product=Vpc&api=CreateIPv6TranslatorEntry)】在线调试，API Explorer 提供在线调用 API、动态生成 SDK Example 代码和快速检索接口等能力，能显著降低使用云 API 的难度，强烈推荐使用。

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateIPv6TranslatorEntry|要执行的操作。 取值： CreateIPv6TranslatorEntry

 |
|AllocateIpv6Port|Integer|是|80|IPv6转换服务实例分配的IPv6地址的使用端口。

 |
|BackendIpv4Addr|String|是|46.22.xx.xx|需要提供IPv6服务的公网IPv4地址（IPv4-only的服务器的IPv4地址）。

 |
|BackendIpv4Port|Integer|是|80|需要提供IPv6服务的公网IPv4地址的端口。

 |
|Ipv6TranslatorId|String|是|ipv6trans-bp1858ys57xxxxxx|IPv6转换服务的实例ID。

 |
|RegionId|String|是|cn-hangzhou|IPv6转换服务实例的地域。 您可以通过调用**DescribeRegions**接口获取地域ID。

 |
|TransProtocol|String|是|tcp|协议类型。取值：

 -   **tcp**：转发TCP协议的报文。
-   **udp**：转发UDP协议的报文。

 |
|AclId|String|否|ipv6transacl-bp1g8bhrdexnrxxxx|关联的访问控制策略组ID。

 |
|AclStatus|String|否|on|是否开启访问控制。取值：**on|off**。

 |
|AclType|String|否|white|是否开启访问控制：

 -   **white**：允许访问策略组中的IPv6地址访问后端服务。
-   **black**：禁止访问策略组中的IPv6地址访问后端服务。

 |
|EntryBandwidth|Integer|否|2|IPv6转换映射条目的带宽峰值。取值：

 -   -1（默认值）：不限制IPv6转换映射条目的带宽峰值。
-   1-200Mbps：改映射条目的带宽值。

 **说明：** 所有IPv6转换映射条目的带宽峰值之和不能超过实例的带宽峰值。

 |
|EntryDescription|String|否|description|IPv6转换映射条目的描述。

 |
|EntryName|String|否|name1|IPv6转换映射条目的名称。长度为 2-100个字符，必须以字母或中文开头，可包含数字，点号（.），下划线（\_）和短横线（-）。但不能以http:// 或https://开头。

 |

## 返回参数 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|DCE5D25-FFC9-492A-8371-12A4E0EE2E05|请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

https://vpc.aliyuncs.com/?Action=CreateIPv6TranslatorEntry
&RegionId=cn-hangzhou
&Ipv6TranslatorId=ipv6trans-bpffafafer55363
&AllocateIpv6Port=80
&BackendIpv4Addr=30.0.0.1
&BackendIpv4Port=80
&TransProtocol=udp
&公共请求参数

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<CreateIPv6TranslatorEntryResponse>
  <Ipv6TranslatorEntryId>ipv6transentry-bp1gpgeb3umme48ygihhg</Ipv6TranslatorEntryId>
  <RequestId>2DCE5D25-FFC9-492A-8371-12A4E0EE2E05</RequestId>
</CreateIPv6TranslatorEntryResponse>

```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"2DCE5D25-FFC9-492A-8371-12A4E0EE2E05",
	"Ipv6TranslatorEntryId":"ipv6transentry-bp1gpgeb3umme48ygihhg"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|403|Forbbiden.SubUser|User not authorized to operate on the specified resource as your account is created by another user.|您没有权限操作该资源，请您申请操作权限后再试。|
|403|Forbidden|User not authorized to operate on the specified resource.|您没有权限操作指定资源，请提交工单咨询。|
|400|Resource.QuotaFull|The quota of resource is full|资源配额已达上限。|

[查看本产品错误码](https://error-center.aliyun.com/status/product/Vpc)

