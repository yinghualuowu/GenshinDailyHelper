<h1 align="center">

GenshinDailyHelper[暂不可用，等待回来~]

</h1>

**原神的签到福利是需要单独下载APP进行才可以领取，并且每天需要打卡，虽然奖励并不是很可观，但有一些摩拉，食材和可观的经验书累计起来还是挺有吸引力的。可能本身不怎么刷论坛的玩家往往会忽略这些奖励。利用Github的Action实现了自动签到功能**

自动签到步骤为
* **获取账号信息（区域和UID）**
* **判断是否已经完成签到**
* **未进行签到到执行签到动作**
* **上述任何步骤出现异常都将判定为失败，并通过Github邮件提醒**

运行结果
![运行图示](https://cdn.jsdelivr.net/gh/yinghualuowu/SakuraWallpaper@74c46f44/cnblog/head/genshin/buildsuccess.png)

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

### 1.3 第三步, 添加Cookie到Secrets
- 在自己的项目界面，点击 ```Settings-->Secrets-->New secret```
![Secrets所在位置](https://cdn.jsdelivr.net/gh/yinghualuowu/SakuraWallpaper@74c46f44/cnblog/head/genshin/setting.png)
- 创建```Cookie```，把第一步保存的```cookie```信息复制到```Value```中

### 1.4 启动Action
- Fork的项目是不会自动运行Action的，需要手动执行一次。
- 点击```Action``` -> ```图1.4.1``` -> ```图1.4.2``` -> ```Run workflow```
![图1.4.1](https://cdn.jsdelivr.net/gh/yinghualuowu/SakuraWallpaper@74c46f44/cnblog/head/genshin/understandflow.png)
![图1.4.2](https://cdn.jsdelivr.net/gh/yinghualuowu/SakuraWallpaper@74c46f44/cnblog/head/genshin/enableflow.png)
![图1.4.3](https://cdn.jsdelivr.net/gh/yinghualuowu/SakuraWallpaper@74c46f44/cnblog/head/genshin/runflow.png)

### 1.5 运行结果
- 运行结果可以点击每一次的执行 -> ```build``` -> ```Run```
![运行结果](https://cdn.jsdelivr.net/gh/yinghualuowu/SakuraWallpaper@74c46f44/cnblog/head/genshin/buildflow.png)

### 其他
- 点击 ```Run workflow```可以手动触发Action
- 自动签到时间是 6点
- 若Cookie失效在第三步替换自己的Cookie。一般情况下Cookie能保持有效期很久。
- 多个账号以```#```隔开，如Cookie1#Cookie2#Cookie3

## 传送门
- https://github.com/y1ndan/genshin-impact-helper 以后一般会根据这个大佬的项目来跟进
