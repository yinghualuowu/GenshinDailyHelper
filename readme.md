<h1 align="center">

GenshinDailyHelper

</h1>

**利用Github的Action最近比较严格，暂不提供执行脚本，该项目会直接采用云函数或docker方式部署**

**原神的签到福利是需要单独下载APP进行才可以领取，并且每天需要打卡，虽然奖励并不是很可观，但有一些摩拉，食材和可观的经验书累计起来还是挺有吸引力的。可能本身不怎么刷论坛的玩家往往会忽略这些奖励。**

自动签到步骤为
* **获取账号信息（区域和UID）**
* **判断是否已经完成签到**
* **未进行签到到执行签到动作**

重要提示

**该项目支持多号签到/多角色签到，但各位旅行者爱惜羊角包，不要滥用**

**如果可以的话，左上角的```Star```顺便点一下吧 > 3 <**

## 使用方法
签到是通过接口模拟请求达成目的，因此需要cookie信息来作为第一步

### 1.1 第一步，获取自己的Cookie信息
- 通过浏览器登录米哈游论坛 https://bbs.mihoyo.com/ys/
- 按```F12```，打开```开发者工具 -> Network``` 点击进入
- 刷新网页，找到以下的位置,复制Cookie后放在记事本或其它可以保存的地方
![Cookie所在位置](https://cdn.jsdelivr.net/gh/yinghualuowu/SakuraWallpaper@74c46f44/cnblog/head/genshin/cookie.png)

### 1.2 第二步，Fork仓库
- 项目地址 ：https://github.com/yinghualuowu/GenshinDailyHelper
- 点击右上角的Fork按钮

## 传送门
- https://github.com/y1ndan/genshinhelper 以后一般会根据这个大佬的项目来跟进

## Star统计
[![Stargazers over time](https://starchart.cc/yinghualuowu/GenshinDailyHelper.svg)](https://starchart.cc/yinghualuowu/GenshinDailyHelper)
