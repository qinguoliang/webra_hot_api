

<p align="center">
  <a href="https://webra.top" target="_blank"><img src="https://github.com/wiuid/webra_hot_api/assets/61615298/554ab508-c376-4f4f-b67f-ed726599caf4" alt="webra_top_api_logo" width="80" /></a>
  <br>
  <span style="font-size: 24px;"><strong>webra_hot_api</strong></span>
</p>
<h3 align="center">热门网站的热榜API</h3>





# 简介
🟢 免部署，直接使用。上手简单。

⛔ 注意，编译程序需要**GLIBC_2.28**支持，可通过 `strings /lib64/libc.so.6  | egrep ^GLIBC_` 命令进行查询，升级安装请自行百度、谷歌

⚠️ 如果想缩短爬取数据的时间（用于达到与对应网站数据的实时性），建议配合代理ip来使用，我这里没有推荐，我用的一家已经关闭了，如果有合适的可以给我推一推，谢谢(/ω＼)

⚠️ 52论坛如果不挂代理，被封ip的概率很大，可能我爬取的时候模拟的信息不到位，目前我代码中使用了一个免费的代理ip，有概率访问失败。

# 接口列表
| 接口地址             | 接口说明             |状态|
| -------------------- | -------------------- |------------|
| IP:5000/wuai         | 吾爱破解的人气热门   |✅|
| ip:5000/zhihu        | 知乎热榜             |✅|
| ip:5000/bili/day     | bilibili全站日榜     |✅|
| ip:5000/bili/hot     | bilibili热搜榜       |✅|
| ip:5000/acfun        | afcun热榜            |✅|
| ip:5000/hupu         | 虎扑热榜             |✅|
| ip:5000/smzdm        | 什么值得买热榜       |✅|
| ip:5000/weibo        | 微博热榜             |✅|
| ip:5000/tieba        | 贴吧热议榜           |✅|
| ip:5000/weixin       | 这个接口不能用       |❌|
| ip:5000/ssp          | 少数派热榜           |✅|
| ip:5000/36k/renqi    | 36氪人气榜           |✅|
| ip:5000/36k/zonghe   | 36氪综合榜           |✅|
| ip:5000/36k/shoucang | 36氪收藏榜           |✅|
| ip:5000/baidu        | 百度热榜             |✅|
| ip:5000/douyin       | 抖音热榜             |✅|
| ip:5000/csdn         | CSDN热榜             |✅|
| ip:5000/history      | 历史上的今天（魔法） |✅|
| ip:5000/douban       | 豆瓣新片榜           |✅|
| ip:5000/ghbk         | 果核剥壳             |✅|
|ip:5000/it/day                |    IT之家_日榜| ✅|
|ip:5000/it/week               |     IT之家_周榜| ✅|
|ip:5000/it/hot                |    IT之家_热评榜| ✅|
|ip:5000/it/month              |      IT之家_月榜| ✅|
|ip:5000/tencent               |    腾讯新闻热点榜| ✅|
|ip:5000/wxbook/soar           |         微信读书_飙升榜| ✅|
|ip:5000/wxbook/new            |        微信读书_新书榜| ✅|
|ip:5000/wxbook/god            |        微信读书_神作榜| ✅|
|ip:5000/wxbook/novel          |          微信读书_小说榜| ✅|
|ip:5000/wxbook/hot            |        微信读书_热搜榜| ✅|
|ip:5000/wxbook/potential      |              微信读书_潜力榜| ✅|
|ip:5000/wxbook/all            |        微信读书_总榜| ✅|
|ip:5000/qidian/yuepiao        |            起点中文网_月票榜| ✅|
|ip:5000/qidian/changxiao      |              起点中文网_畅销榜| ✅|
|ip:5000/qidian/zhisu          |          起点中文网_阅读指数榜| ✅|
|ip:5000/qidian/tuijina        |            起点中文网_推荐榜| ✅|
|ip:5000/qidian/shoucang       |             起点中文网_收藏榜| ✅|
|ip:5000/qidian/new            |        起点中文网_签约作者新书榜| ✅|
|ip:5000/qidian/new_2          |          起点中文网_公众作家新书榜| ✅|
|ip:5000/qidian/yuepiao_vip    |                起点中文网_月票_VIP榜| ✅|
|ip:5000/zongheng/yuepiao      |              纵横中文网_月票榜| ✅|
|ip:5000/zongheng/24h          |          纵横中文网_24h畅销榜| ✅|
|ip:5000/zongheng/new          |          纵横中文网_新书榜| ✅|
|ip:5000/zongheng/tuijian      |              纵横中文网_推荐榜| ✅|
|ip:5000/zongheng/new_dingyue  |                  纵横中文网_新书订阅榜| ✅|
|ip:5000/zongheng/dianji       |             纵横中文网_点击榜| ✅|

# 部署方法
## 1、github发版使用方法

- 😆 发版使用pyinstaller 进行打包，不太了解这些东西，以后再研究研究怎么把包的大小搞下去

```shell
# 将下载下来的webra_top.zip 进行解压缩
unzip webra_top.zip
cd webra_top
# 赋予执行权限，init是用shell语句写的
chmod +x init

./init
Usage: ./init.sh {start|stop|restart|status}
# 启动
./init start
# 关闭
./init stop
# 重启
./init restart
# 查看状态
./init status

# 查看端口监听是否存在
ss -tanpl
State                 Recv-Q                Send-Q                               Local Address:Port                               Peer Address:Port               Process                                         
LISTEN                0                     128                                      127.0.0.1:5000                                    0.0.0.0:*                   users:(("top",pid=106379,fd=3))                

# 测试正常运行
curl 127.0.0.1:5000/zhihu

```

返回数据结构如下

```json
{
  "secure":true,
  "title":"知乎热榜",
  "update_time":"2024-01-24 21:25:42",
  "data":[
    {
    "index":1,
    "title":"腾讯以 64.2 亿元拿下北京海淀区地块，如何看待此举？",
    "url":"https://www.zhihu.com/question/640924601",
    "hot":"1156W"
    },
    {
    "index":2,
    "title":"江西新余一楼房发生火灾，已致 39 人遇难，目前情况如何？",
    "url":"https://www.zhihu.com/question/641016841",
    "hot":"356W"
    },
    {}
  ]
}
```


## 2、代码使用方法
https://www.webra.top/1371.html

![image](https://github.com/wiuid/webra_hot/assets/61615298/560b52ea-94f6-4e92-829e-124791e39042)


