# 梨视频 #
- [列表获取](#listGet)
- [首页](#home)
	- [头条](#head)
	- [头条详细内容](#head_details)

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
	- `contList`：详细内容
		- `contId`：详细内容 id，用作查看[头条详细内容](#head_details)
		- `name`：标题
		- `pic`：图片 url
		- `nodeInfo`：
			- `name`：作者名
		- `duration`：时长
		- `cornerLabel`：视频类型代码
		- `cornerLabelDesc`：视频类型描述
		- `coverVideo`：视频播放地址
		- `praiseTimes`：点赞量

<h3 id="head_details">头条详细内容</h3>

url：http://app.pearvideo.com/clt/jsp/v2/content.jsp

拼接参数：

- `contId`：从[头条](#head) json 中 `contId` 字段获取到的值

url 示例：[`http://app.pearvideo.com/clt/jsp/v2/content.jsp?contId=1064146`](http://app.pearvideo.com/clt/jsp/v2/content.jsp?contId=1064146)

json 示例：

	{
      "resultCode": "1",
      "resultMsg": "success",
      "reqId": "215d100a-d167-47ee-8d27-fab609b36934",
      "systemTime": "1492153703690",
      "areaList": [
        {
          "area_id": "200008",
          "expInfo": {
            "algorighm_exp_id": "",
            "front_exp_id": "0",
            "s_value": "8f8a74f4-d7bc-41f9-b442-1e5f74622f9b_2088549785888668"
          }
        }
      ],
      "content": {
        "contId": "1064146",
        "name": "她收养40流浪猫:让它们有尊严活着",
        "summary": "辽宁沈阳，73岁老太孔德荣，是远近闻名的“猫奶奶”，10年收养流浪猫40余只，月花销上千元，她说服儿子让出车库给猫咪住，想让它们活得有尊严。",
        "source": "",
        "pubTime": "2017-04-14 12:53",
        "isVr": "0",
        "aspectRatio": "0",
        "contentHtml": "",
        "liveHtml": "",
        "postHtml": "http://app.pearvideo.com/clt/page/v2/topic_comm.jsp?postId=1047857&type=living",
        "praiseTimes": "266",
        "commentTimes": "3",
        "isFavorited": "0",
        "pic": "http://image2.pearvideo.com/cont/20170414/cont-1064146-10255376.png",
        "postId": "1047857",
        "liveRoomId": "",
        "sharePic": "http://image.pearvideo.com/cont/20170414/cont-1064146-10255377.png",
        "shareUrl": "http://www.pearvideo.com/detail_1064146",
        "liveInfo": {},
        "cornerLabel": "3",
        "cornerLabelDesc": "独播",
        "authors": [
          {
            "userId": "10265801",
            "nickname": "泛    舟",
            "isPaike": "1",
            "paikeType": "1"
          }
        ],
        "tags": [
          {
            "tagId": "1365",
            "name": "老人"
          },
          {
            "tagId": "5390",
            "name": "好心人"
          },
          {
            "tagId": "15721",
            "name": "流浪猫"
          }
        ],
        "videos": [
          {
            "videoId": "10369556",
            "url": "http://video.pearvideo.com/mp4/short/20170414/cont-1064146-10369519-ld.mp4",
            "tag": "ld",
            "format": "mp4",
            "fileSize": "5913937",
            "duration": "117"
          },
          {
            "videoId": "10369557",
            "url": "http://video.pearvideo.com/mp4/short/20170414/cont-1064146-10369519-fhd.mp4",
            "tag": "fhd",
            "format": "mp4",
            "fileSize": "36734910",
            "duration": "117"
          },
          {
            "videoId": "10369558",
            "url": "http://video.pearvideo.com/mp4/short/20170414/cont-1064146-10369519-sd.mp4",
            "tag": "sd",
            "format": "mp4",
            "fileSize": "10265849",
            "duration": "117"
          },
          {
            "videoId": "10369559",
            "url": "http://video.pearvideo.com/mp4/short/20170414/cont-1064146-10369519-hd.mp4",
            "tag": "hd",
            "format": "mp4",
            "fileSize": "19314179",
            "duration": "117"
          }
        ],
        "nodeInfo": {
          "nodeId": "25",
          "name": "一手Video",
          "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg",
          "isOrder": "0",
          "desc": "千万拍客为你现场播报"
        },
        "copyright": "版权声明：本内容系梨视频独家，未经授权，不得转载",
        "isDownload": "1",
        "duration": "01'57\"",
        "adMonitorUrl": ""
      },
      "nextInfo": {
        "contId": "1060885",
        "name": "车祸现场交警脱衣，上演温馨一幕",
        "forwordType": "1"
      },
      "postInfo": {
        "postId": "1047857",
        "name": "“猫奶奶”十年收养40多只流浪猫",
        "commentTimes": "3",
        "communityInfo": {
          "communityId": "12",
          "name": "露一手",
          "logoImg": "http://imageugc2.pearvideo.com/community/12-10001210-logo.jpg"
        },
        "isfavorited": "0",
        "postHtml": "http://app.pearvideo.com/clt/page/v2/topic_comm.jsp?postId=1047857&contId=1064146",
        "childList": [
          {
            "commentId": "10324796",
            "content": "好人有好报！",
            "pubTime": "04-14 13:03",
            "topTimes": "1",
            "stepTimes": "2",
            "replyTimes": "0",
            "userInfo": {
              "userId": "10246234",
              "nickname": "鱼小胖",
              "isPaike": "0",
              "pic": "http://imageugc.pearvideo.com/user/20170214/10246234-210230.jpg"
            }
          },
          {
            "commentId": "10324982",
            "content": "对待流浪猫最好的方式是抓捕——绝育——放归，对流浪猫来说这样都关在笼子里就有尊严了么",
            "pubTime": "04-14 14:04",
            "topTimes": "0",
            "stepTimes": "0",
            "replyTimes": "0",
            "userInfo": {
              "userId": "10091535",
              "nickname": "刘面瘫",
              "isPaike": "0",
              "pic": "http://imageugc.pearvideo.com/user/20161224/10091535-123600.jpg"
            }
          },
          {
            "commentId": "10324977",
            "content": "人为出名无所不能",
            "pubTime": "04-14 13:56",
            "topTimes": "0",
            "stepTimes": "0",
            "replyTimes": "0",
            "userInfo": {
              "userId": "10558703",
              "nickname": "良",
              "isPaike": "0",
              "pic": "http://imageugc.pearvideo.com/user/20170413/10558703-213237.jpg"
            }
          }
        ]
      },
      "relateConts": [
        {
          "contId": "1060885",
          "name": "车祸现场交警脱衣，上演温馨一幕",
          "pic": "http://image2.pearvideo.com/cont/20170408/cont-1060885-10241849.png",
          "nodeInfo": {
            "nodeId": "25",
            "name": "一手Video",
            "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "3",
          "cornerLabelDesc": "独播",
          "forwordType": "1",
          "videoType": "1",
          "duration": "00'51\"",
          "liveStatus": "",
          "praiseTimes": "63"
        },
        {
          "contId": "1054359",
          "name": "感动！他竟然是这样给猫过生日的！",
          "pic": "http://image1.pearvideo.com/cont/20170327/cont-1054359-10215505.png",
          "nodeInfo": {
            "nodeId": "189",
            "name": "上海街头",
            "logoImg": "http://image1.pearvideo.com/node/189-10070077-logo.png"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "04'12\"",
          "liveStatus": "",
          "praiseTimes": "20"
        },
        {
          "contId": "1017920",
          "name": "理发只收1元，老人坚持了23年",
          "pic": "http://image2.pearvideo.com/cont/20161222/cont-1017920-10075253.jpg",
          "nodeInfo": {
            "nodeId": "9",
            "name": "微辣Video",
            "logoImg": "http://image2.pearvideo.com/node/9-10027910-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "",
          "cornerLabelDesc": "",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'05\"",
          "liveStatus": "",
          "praiseTimes": "5"
        },
        {
          "contId": "1019106",
          "name": "老人除雪17年，因儿子雪天车祸离世",
          "pic": "http://image1.pearvideo.com/cont/20161227/cont-1019106-10080103.png",
          "nodeInfo": {
            "nodeId": "25",
            "name": "一手Video",
            "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "3",
          "cornerLabelDesc": "独播",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'42\"",
          "liveStatus": "",
          "praiseTimes": "42"
        },
        {
          "contId": "1046947",
          "name": "他流浪一生，88岁终于住进敬老院",
          "pic": "http://image2.pearvideo.com/cont/20170313/cont-1046947-10186541.png",
          "nodeInfo": {
            "nodeId": "25",
            "name": "一手Video",
            "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "5",
          "cornerLabelDesc": "推荐",
          "forwordType": "1",
          "videoType": "1",
          "duration": "01'04\"",
          "liveStatus": "",
          "praiseTimes": "93"
        },
        {
          "contId": "1062475",
          "name": "拾荒老父再流浪:捡瓶换馍,不找女儿",
          "pic": "http://image1.pearvideo.com/cont/20170411/cont-1062475-10248622.png",
          "nodeInfo": {
            "nodeId": "25",
            "name": "一手Video",
            "logoImg": "http://image.pearvideo.com/node/25-10027890-logo.jpg"
          },
          "link": "http://",
          "linkType": "0",
          "cornerLabel": "3",
          "cornerLabelDesc": "独播",
          "forwordType": "1",
          "videoType": "1",
          "duration": "02'54\"",
          "liveStatus": "",
          "praiseTimes": "5428"
        }
      ]
    }

json 解析：

- `resultCode`：为`1`时表请求成功
- `content`：视频具体内容
	- `name`：视频标题
	- `summary`：视频描述
	- `pubTime`：视频上传时间
	- `tags`：标签
	- `relateConts`：相关视频
	- `postInfo`：其他信息
		- `childList`：评论信息
			- `commentId`：评论 id
			- `content`：评论内容
			- `pubTime`：评论时间
			- `topTimes`：顶的数量
			- `stepTimes`：踩的数量
			- `userInfo`：评论者信息
			- `replyTimes`：回复评论的数量
		- `videos`：各个版本视频连接
			- `url`：视频地址
			- `tag`：视频清晰度
			- `duration`：视频时长
			- `fileSize`：视频大小