# describeLiveDomain


## 描述
查询域名列表

## 请求方式
GET

## 请求地址
https://live.jdcloud-api.com/v1/domains


## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**filters**|Filter[]|False| |域名列表查询过滤条件, 不传递分页参数时默认返回10条|
|**pageNum**|Integer|False|1|页码；默认为1|
|**pageSize**|Integer|False|10|分页大小；默认为10；取值范围[10, 100]|

### Filter
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**name**|String|True| |过滤条件的名称|
|**operator**|String|False| |过滤条件的操作符，默认eq|
|**values**|String[]|True| |过滤条件的值|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|ruquestId|
|**result**|Result| |

### Result
|名称|类型|描述|
|---|---|---|
|**domainList**|DomainList[]|域名集合|
|**pageNumber**|Integer|当前页码|
|**pageSize**|Integer|每页数量|
|**totalCount**|Number|查询总数|
### DomainList
|名称|类型|描述|
|---|---|---|
|**playDomain**|PlayDomain[]|直播域名集合|
|**publishDomain**|PublishDomain[]|推流域名集合|
### PlayDomain
|名称|类型|描述|
|---|---|---|
|**createTime**|String|创建时间|
|**domainStatus**|String|直播域名状态|
|**playDomain**|String|播放域名|
|**playDomainCname**|String|播放域名(Cname)|
|**regionId**|String|地域编码|
|**updateTime**|String|更新时间|
### PublishDomain
|名称|类型|描述|
|---|---|---|
|**createTime**|String|创建时间|
|**domainStatus**|String|直播域名状态|
|**publishDomain**|String|推流域名|
|**publishDomainCname**|String|推流域名(Cname)|
|**regionId**|String|地域编码|
|**updateTime**|String|更新时间|

## 返回码
|返回码|描述|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|