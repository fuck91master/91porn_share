# 91porn_share
91porn api免费分享 纯公益和练手
# 特别注意
由于有个傻逼攻击服务器，估计是动了人家蛋糕了  
因此今后请求video_url的时候需要进行鉴权   
有需要的可以发邮件fuck91master@protonmail.ch获取key,
如果请求频率比较高，可以把ip同时发给我，取消限制     
如果发现key被恶意使用，将会取消授权  
服务器太渣，请轻点虐
# API版接口 

获取视频列表接口: https://api.zhaiclub.com/source/source_list  
获取视频播放地址接口:http://down.zhaiclub.com/

## 接口：获取视频列表
| 描述     | 内容               |
| -------- | ------------------ |
| 接口功能 | 请求91porn视频资源 |
| 请求协议 | HTTPS              |
| 请求方法 | GET                |
| 请求url  | source_list           |
| 响应格式 | json               |

### 请求参数

| 参数     | 描述                                             | 必填 | 类型   |
| -------- | ------------------------------------------------| ---- | ------ |
| viewkey  | 视频播放id                                       | 否  | string    |
| limit    |每页显示数量                                            | 否  | int    |
| page     | 页码                                            | 否  | int    |
| title    | 标题（支持模糊搜索）                               | 否  | string   |
| author   | 作者（支持模糊搜索）                                | 否  |  string   |
| vid      |视频id                                              | 否  |  string   |
| up_time  |上传时间                                             | 否  | string   |
| view     | 观看次数  | 否   | String |
| favorites | 收藏次数  | 否   | String |
| comment   | 评论次数  | 否   | String |
| integral | 积分  | 否   | String |
| order    | 排序(想要排序的字段)  | 否   | String |
| att      | desc和asc二选一,默认desc  | 否   | String |


### 响应参数

| 参数        | 描述                     | 必有 | 类型          |
| ----------- | ------------------------ | ---- | ------------- |
| status   | 状态码                   | 是   | String        |
| msg | 状态消息                   | 是   | String        |
| count| 总数         | 是   | String        |
| data | 视频列表，object格式见下 | 是   | Array[Object] |


data object结构,如下：

| 参数       | 描述        | 必有 | 类型   |
| ---------- | ----------- | ---- | ------ |
| viewkey    | 视频viewkey | 是   | String |
| img      | 视频图片    | 是   | String |
| author        | 作者 | 是   | String |
| up_time   | 上传时间    | 是   | String |
| title   | 视频标题    | 否   | String |
| vid | 视频id    | 是   | String |
| duration | 视频长度  | 是   | String |
| view | 观看次数  | 是   | String |
| favorites | 收藏次数  | 是   | String |
| comment | 评论次数  | 是   | String |
| integral | 积分  | 是   | String |
| video_url | 视频地址  | 是   | String |

### 请求示例

```
https://api.zhaiclub.com/source/source_list?title=电话
```

### 响应示例


```
{
    "status": "200",
    "msg": "返回成功",
    "data": {
        "list": [
            {
                "viewkey": "059b36612c5ab4adb070",
                "image": "https://img.t6k.co/thumb/386264.jpg",
                "author": "Zyusn99_  ",
                "up_time": "2020-07-30",
                "title": "操着接老公电话，差点被听出来，对话刺激，已婚少妇的快乐！",
                "vid": "386264",
                "duration": "09:16",
                "view": "113 ",
                "favorites": "1",
                "comment": "0 ",
                "integral": "0",
                "video_url": "https://down.zhaiclub.com/386264.mp4"
            }
}
```
## 接口：获取视频真实地址
| 描述     | 内容               |
| -------- | ------------------ |
| 接口功能 | 请求91porn视频真实地址 |
| 请求协议 | HTTPS              |
| 请求方法 | GET                |
| 响应格式 | json               |

### 请求参数

| 参数     | 描述                                             | 必填 | 类型   |
| -------- | ------------------------------------------------ | ---- | ------ |
| key     | 授权码（发邮件申请）                                             | 否  | string    |
| act     | 操作行为（默认传url）                                            | 否  | string   |



### 响应参数

| 参数        | 描述                     | 必有 | 类型          |
| ----------- | ------------------------ | ---- | ------------- |
| status   | 状态码                   | 是   | String        |
| msg | 状态消息                   | 是   | String        |
| data | 视频真实访问地址（2小时有效）| 是   | String |

### 请求示例

```
https://down.zhaiclub.com/386809.mp4?key=XXX&act=url
```

```
{
    "code": 10000,
    "msg": "请求成功",
    "data": "https://down.zhaiclub.com/386809.mp4&ticket=3d8a1e84a4c593278492083143cc94b2"
}
```

### 服务器成本比较高,有钱捧个钱场,没钱的捧个人场

```
BTC:1CuUZZEDhG4SzcwHu9GgaTGm1bbvX2e4cp

```
![Image text](https://github.com/fuck91master/91porn_share/blob/master/BTC.jpg)


