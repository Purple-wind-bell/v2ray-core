## v2ray 最新版本

[![](https://images.microbadger.com/badges/version/mritd/v2ray.svg)](https://microbadger.com/images/mritd/v2ray "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/mritd/v2ray.svg)](https://microbadger.com/images/mritd/v2ray "Get your own image badge on microbadger.com")

> 截至目前该镜像为 v2ray 最新版本

### 安装
  docker pull wj1323246431/v2ray
  docker run -d --name v2ray -p 8888:10000 wj1323246431/v2ray
  
注意： config.json文件本文件夹目录下。

``` sh

```

**Container 内部默认监听 10000 端口**
**v2ray 默认 ID 为 `89be7f2e-138b-4343-9823-b57ae12ab90d`(不保证后期变动)**

### 自定义配置

**镜像支持写入自定义的 v2ray 配置，挂载覆盖 `/etc/v2ray/config.json` ，例如：

docker run -d --name v2ray -p 8888:10000 -v /etc/v2ray:/etc/v2ray wj1323246431/v2ray

其中，1--- -v /etc/v2ray:/etc/v2ray 表示外部文件夹映射容器内部文件夹，可在创建容器前将配置文件放置于/etc/v2ray目录下，文件名为config.json.

2--- -p 8888:10000 表示主机8888端口绑定容器10000端口，10000端口在config.json文件中设置。

3--- 如果使用nginx代理，需要将端口映射设置为-p 127.0.0.1:8888:10000,nginx流量转发到127.0.0.1:8888.

### 样例配置

**镜像使用官方的样例配置，来源于官方发布包，可执行以下命令获取样例配置**
**具体修改设置请参考 [官方文档配置部分](https://www.v2ray.com/chapter_02/)**

