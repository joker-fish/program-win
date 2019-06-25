## 新建用户并返回等待状态

1.请求地址：http://tianqi.815ff.com/api/data/createUser

2.请求方式：get

3.请求参数：

|名称|类型|说明|
| --- |:---:|---:|
|package|string|安装包名|

失败：

```

```


成功：

```
[
    {
        "code": "101",
        "msg": "进入等待",
        "data": {
            "time" => 13
        }
    },
    {
        "code": "102",
        "msg": "直接安装"
    }
]
```


4.数据说明：

|名称|类型|说明|
| --- |:---:|---:|
|time|int|分配时间段|

## 上传电脑数据

1.请求地址：http://tianqi.815ff.com/api/data/index

2.请求方式：get

3.请求参数：

|名称|类型|说明|
| --- |:---:|---:|
|disk|string|硬盘序列号|
|ip|string|ip地址|
|mac|string|mac地址|
|mainboard|string|主板信息|
|package|string|安装包名|

失败：

```
[
    {
        "code": "101",
        "msg": "该数据已存在"
    }
]
```


成功：

```
{
    "code": "200",
    "msg": "上传成功"
}
```


4.数据说明：

|名称|类型|说明|
| --- |:---:|---:|

## 安装成功更改安装状态

1.请求地址：http://tianqi.815ff.com/api/data/changeStatus

2.请求方式：get

3.请求参数：

|名称|类型|说明|
| --- |:---:|---:|
|disk|string|硬盘序列号|
|ip|string|ip地址|
|mac|string|mac地址|
|mainboard|string|主板信息|
|package|string|安装包名|
|status|int|状态（传：1）|

失败：

```
[
    {
        "code": "101",
        "msg": "status请传1"
    }
]
```


成功：

```
{
    "code": "200",
    "msg": "修改成功"
}
```


4.数据说明：

|名称|类型|说明|
| --- |:---:|---:|

## 查询是否允许安装

1.请求地址：http://tianqi.815ff.com/api/data/install

2.请求方式：get

3.请求参数：

|名称|类型|说明|
| --- |:---:|---:|

失败：

```

```


成功：

```
[
    {
        "code": "101",
        "msg": "不允许安装"
    },
    {
        "code": "200",
        "msg": "允许安装"
    }
]
```


4.数据说明：

|名称|类型|说明|
| --- |:---:|---:|

