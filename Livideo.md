# 梨视频 #
<h2 id="listGet">列表获取</h2>
url：[`http://app.pearvideo.com/clt/jsp/v2/domainList.jsp?type=ALL`](http://app.pearvideo.com/clt/jsp/v2/domainList.jsp?type=ALL)

请求方式：GET

json 示例：

	{
      "resultCode": "1",
      "resultMsg": "success",
      "reqId": "9de2e3fc-46d7-4341-8997-5c773678ea85",
      "systemTime": "1492152517376",
      "sex": "",
      "domainList": [
        {
          "domainId": "5",
          "name": "资讯",
          "selected": "0"
        },
        {
          "domainId": "8",
          "name": "娱乐",
          "selected": "0"
        },
        {
          "domainId": "12",
          "name": "社会",
          "selected": "0"
        },
        {
          "domainId": "22",
          "name": "美食",
          "selected": "0"
        },
        {
          "domainId": "21",
          "name": "搞笑",
          "selected": "0"
        },
        {
          "domainId": "2",
          "name": "科技",
          "selected": "0"
        },
        {
          "domainId": "1",
          "name": "体育",
          "selected": "0"
        },
        {
          "domainId": "13",
          "name": "财经",
          "selected": "0"
        },
        {
          "domainId": "3",
          "name": "军事",
          "selected": "0"
        },
        {
          "domainId": "7",
          "name": "知识",
          "selected": "0"
        },
        {
          "domainId": "9",
          "name": "生活",
          "selected": "0"
        },
        {
          "domainId": "25",
          "name": "时尚",
          "selected": "0"
        },
        {
          "domainId": "15",
          "name": "文化",
          "selected": "0"
        },
        {
          "domainId": "20",
          "name": "情感",
          "selected": "0"
        },
        {
          "domainId": "23",
          "name": "创意",
          "selected": "0"
        },
        {
          "domainId": "14",
          "name": "历史",
          "selected": "0"
        },
        {
          "domainId": "38",
          "name": "汽车",
          "selected": "0"
        },
        {
          "domainId": "24",
          "name": "旅行",
          "selected": "0"
        },
        {
          "domainId": "4",
          "name": "健康",
          "selected": "0"
        },
        {
          "domainId": "26",
          "name": "亲子",
          "selected": "0"
        },
        {
          "domainId": "27",
          "name": "萌宠",
          "selected": "0"
        },
        {
          "domainId": "19",
          "name": "人物",
          "selected": "0"
        },
        {
          "domainId": "30",
          "name": "纪录",
          "selected": "0"
        },
        {
          "domainId": "29",
          "name": "家居",
          "selected": "0"
        },
        {
          "domainId": "28",
          "name": "暖闻",
          "selected": "0"
        }
      ]
    }

json 解析：

<h2 id="home">首页</h2>
<h3 id="head"> 头条 </h3>

url：[`http://app.pearvideo.com/clt/jsp/v2/home.jsp?lastLikeIds=1063871%2C1063985%2C1064069%2C1064123%2C1064078%2C1064186%2C1062372%2C1064164%2C1064081%2C1064176%2C1064070%2C1064019`](http://app.pearvideo.com/clt/jsp/v2/home.jsp?lastLikeIds=1063871%2C1063985%2C1064069%2C1064123%2C1064078%2C1064186%2C1062372%2C1064164%2C1064081%2C1064176%2C1064070%2C1064019)

请求方式：GET

请求头：

| 请求头        | 值           |
| ------------- |:-------------:|
|  X-Channel-Code    | 固定值 `official`，可为空 |
|  X-Client-Agent    | 手机品牌，例如 Xiaomi，可为空 |
|   X-Client-Hash   | 长度为32的小写字母和数字混合字符串，例`2f3d6ffkda95dlz2fhju8d3s6dfges3t`，可为空 |
|   X-Client-ID   | 长度为的15数字字符串，例`123456789123456`，可为空 |
|   X-Client-Version   | 为空即可 |
|   X-Long-Token   | 为空即可 |
|   X-Platform-Type   | 为空即可 |
|   X-Platform-Version   | 为空即可 |
|  X-Serial-Num    | Unix 时间戳 |
|   X-User-ID   | 为空即可 |

请求头示例：

	X-Channel-Code:official
	X-Client-Agent:Xiaomi
	X-Client-Hash:2f3d6ffkda95dlz2fhju8d3s6dfges3t
	X-Client-ID:123456789123456
	X-Client-Version:2.3.2
	X-Long-Token:
	X-Platform-Type:0
	X-Platform-Version:5.0
	X-Serial-Num:1492140134
	X-User-ID:

json 示例：

json 解析：

- `resultCode`：为`1`时表请求成功
- `dataList`：具体数据
	- `nodeName`：所属板块，取值有`头条`、`为你推荐`、`全民拍客活动`、`最新视频`、`娱乐精选`等
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：
	- ``：
- ``：
- ``：
- ``：
- ``：