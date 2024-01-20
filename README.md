

# webra_hot_api
热门网站的热榜API

免部署，直接使用。

注意，如果想缩短爬取数据的时间（已达到与对应网站数据的实时性），建议配合代理ip来使用，我这里没有推荐，我用的一家已经关闭了，如果有合适的可以给我推一推，谢谢(/ω＼)

52论坛如果不挂代理，被封ip的概率很大，可能我爬取的时候模拟的信息不到位，目前我代码中使用了一个免费的代理ip，有概率访问失败。

# github发版使用方法

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

```


# 代码使用方法参考
https://www.webra.top/1371.html

![image](https://github.com/wiuid/webra_hot/assets/61615298/560b52ea-94f6-4e92-829e-124791e39042)


