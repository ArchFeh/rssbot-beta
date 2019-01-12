# RSSBot-beta

# 样例

[Telgram RSS Bot](https://t.me/BRSSBot)

## 命令

|命令|描述|
|:-|:-|
|sub url|订阅一个RSS|
|unsub url|退订一个RSS|
|rss|显示已经订阅的RSS|

## 配置

在项目根目录创建名为`conf.ini`的文件，并填入以下配置

```ini
[default]
# 从BotFather获取的token
token=your-token
# 同一个RSS刷新时间间隔，单位为秒
# RSS的刷新平均分布到这段时间间隔中
# 例如，存在两个订阅，则分别在0时刻和150时刻刷新
freq=300
# RSS源可能出现不可获取的情况，
# 连续多次不可获取后，暂停该RSS的推送，
# 并提醒订阅者检查该RSS
errorlimit=60
# 开始使用Bot时的提示提示内容
startmsg=<a href="https://github.com/nierunjie/rssbot-beta/blob/master/README.zh-CN.md">README</a>
# 管理员，用于权限控制，值为username
admin=lanthora
# 非管理员可订阅的数量，设置为0则仅管理员可用
sublimit=10
# 数据库相关文件，修改请慎重
dbname=rss.db
sqlfile=rss.sql
```