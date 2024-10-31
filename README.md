# uptime-status

一个基于 UptimeRobot API 的在线状态面板，fork自[yb/uptime-status](https://github.com/yb/uptime-status)，用来保存自己的自定义设置。



## 事先准备

- 您需要先到 [UptimeRobot](https://uptimerobot.com/ "UptimeRobot") 添加站点监控，并在 [My Settings页面](https://old.uptimerobot.com/dashboard?ref=beta-app#mySettings) 获取 API Key
- 您需要拥有一个网站空间，常见的 Nginx / PHP 等空间即可，甚至是阿里云的 OSS 等纯静态空间也行

## 如何部署：

- 下载并解压缩：[build.zip](https://github.com/insectmk/uptime-status/releases/latest/download/build.zip "build.zip") 
- 修改 `config.js` 文件：
   - `SiteName`: 要显示的网站名称
   - `ApiUrl`: API接口地址，默认[https://api.uptimerobot.com/v2/getMonitors](https://api.uptimerobot.com/v2/getMonitors)
   - `ApiCatchTime`: 缓存时间，单位（ms），默认1分钟
   - `ApiKeys`: 从 UptimeRobot 获取的 API Key，支持 Monitor-Specific API Keys 和 Read-Only API Key
   - `CountDays`: 要显示的日志天数，建议 60 或 90，显示效果比较好
   - `ShowLink`: 是否显示站点链接
   - `Navi`: 导航栏的菜单列表
- 将所有文件上传到网站空间

⚠️ 如果没有修改代码的需求，您不需要 git clone 本项目，只需要下载 [Release](https://github.com/yb/uptime-status/releases) 的文件包即可。

## 个人更新

1. 将时间顺序颠倒，最新数据靠右。
1. 接口数据缓存、自定义接口地址。

