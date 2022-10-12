# 教程
[GitHub - chenjiandongx/bili-spider: 📺 B 站全站视频信息爬虫](https://github.com/chenjiandongx/bili-spider)

# b站视频搜索
默认可对分区和时长进行筛选，
点击/收藏/评论/发布可排序不可筛选
硬币既不可排序也不可筛选
# 最新视频
[bilibili-API-collect/dynamic.md at master · SocialSisterYi/bilibili-API-collect](https://github.com/SocialSisterYi/bilibili-API-collect/blob/master/ranking&dynamic/dynamic.md)
随机/不固定
带有硬币信息
# channel
https://api.bilibili.com/x/web-interface/web/channel/featured/list?channel_id=37242&filter_type=2022&offset=980011163_759773&page_size=30
# 问题
最多查询三个月的时间，但是结果不一定是正确的，如果查询到的结果太多就会筛选。某一个数量。而不是全部显示

# 不需教程
网上的教程又过时又烂，其实b站API除了有频率限制外，根本没什么反爬机制，直接看浏览器请求，照着格式掉用就行。
[python爬虫实战(十) B站热门视频信息爬取（简易版）| API接口爬取_shine4869的博客-CSDN博客](https://blog.csdn.net/shine4869/article/details/111407476)

# API
[SocialSisterYi/bilibili-API-collect: 哔哩哔哩-API收集整理【不断更新中....】](https://github.com/SocialSisterYi/bilibili-API-collect)
	够全
[bilibili-API-collect/search_request.md at master · SocialSisterYi/bilibili-API-collect · GitHub](https://github.com/SocialSisterYi/bilibili-API-collect/blob/master/search/search_request.md)
[bilibili-API-collect 分区最新视频](https://github.com/SocialSisterYi/bilibili-API-collect/blob/master/ranking&dynamic/dynamic.md)
[GitHub - Passkou/bilibili-api: 哔哩哔哩的API调用模块](https://github.com/Passkou/bilibili-api)
	python, 不全
[GitHub - MoyuScript/bilibili-api: 哔哩哔哩的API调用模块](https://github.com/MoyuScript/bilibili-api)
	python, 不全
# 分区id
[随手找的API系列：Bilibili - 哔哩哔哩](https://www.bilibili.com/read/cv6776540/)
[bilibili-API-collect/video_zone.md at master · SocialSisterYi/bilibili-API-collect](https://github.com/SocialSisterYi/bilibili-API-collect/blob/master/video/video_zone.md)
36   知识 
201   科学科普 
124   社科人文 
207   财经
208   校园学习 
209   职业职场 
122   野生技术协会 
188   数码

## 为什么
提供一个替代娱乐的选项
不只看，还可以听
给B站智能推荐提供更好的数据
## 直接看有什么问题
排序方式太原始，单一的播放量|硬币数|收藏数都不能说明质量
页面UI中看不中用
## 怎么解决
更简洁实用的UI
按播放收藏比排序，过滤收藏数过低的
## 难点
直接爬页面数据不够，只有播放数和评论数
官方和第三方都没有能直接用的API
# 实现
一次最多查询100个
# 数据筛选
收藏量太少容易选到过于专业的

# 硬币估算
```
senddate: 1599839631,
rank_offset: 200,
tag: '知识分享官,财经,龙王,奶茶,知识,美食,生活,科普,蜜雪冰城,喜茶',
duration: 515,
id: 372048764,
rank_score: 7856,
badgepay: false,
pubdate: '2020-09-11 11:41:22',
author: '顾均辉要出圈',
review: 4301,
mid: 586462804,
is_union_video: 0,
rank_index: 0,
type: 'video',
arcrank: '0',
play: '752052',
pic: '//i0.hdslb.com/bfs/archive/7a437f2295b8e8f2816add0f0710a1b53b532167.jpg',
description: '原始的就是经典的，平价的就是世界的！',
video_review: 11181,
is_pay: 0,
favorites: 7856,
arcurl: 'http://www.bilibili.com/video/av372048764',
bvid: 'BV1VZ4y1N7Vf',
title: '为什么全国卖得最好的奶茶，是只要4块一杯的蜜雪冰城？'
```

# 发现
通过巧妙的ui设计。让人在看到垃圾内容的时候也没那么反感，反而是选择继续往下刷。

# 筛雪
播放量过于少的。。
时间过于长了。
时间过于短的。
其实播放量过于多的也可以排除掉。没办法借助这个视频发现更多的好视频。

# rank_score
```
//countArcHot 视频=硬币*0.4+收藏*0.3+弹幕*0.4+评论*0.4+播放*0.25+点赞*0.4+分享*0.6 最新视频（一天内发布）提权[总值*1.5]
func countArcHot(t *api.Stat, ptime int64) int64 {
    if t == nil {
        return 0
    }
    hot := float64(t.Coin)*0.4 +
        float64(t.Fav)*0.3 +
        float64(t.Danmaku)*0.4 +
        float64(t.Reply)*0.4 +
        float64(t.View)*0.25 +
        float64(t.Like)*0.4 +
        float64(t.Share)*0.6
    if ptime >= time.Now().AddDate(0, 0, -1).Unix() && ptime <= time.Now().Unix() {
        hot *= 1.5
    }
    return int64(math.Floor(hot))
}
```
分享 > 点赞 = 硬币 ( = 弹幕) = 评论 > 收藏 > 播放/阅读