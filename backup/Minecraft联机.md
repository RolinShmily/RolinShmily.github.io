## 一、工具下载
- 我们使用的工具是 ***ZeroTier***  一个专门用来建立点对点虚拟专用网(***P2P VPN***)
- 以***Windows***系统为例
1. 下载地址：https://www.zerotier.com/

![屏幕截图 2024-06-22 105811](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/d906566c-6819-47f8-a9e6-640b48e43d19)

2. 点击 ***Download***

![屏幕截图 2024-06-22 105945](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/4ea5fbc8-d658-4bff-a5a4-b0c1e6a2e2ca)

3. 一般情况下直接点击 ***MSI Installer (x86/x64)*** 下载完成如图

![屏幕截图 2024-06-22 110219](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/93ee2260-8306-473c-8275-90f648089bc1)

4. 安装前请把 ***杀毒软件*** 全部关闭，尽量不要出现被拦截的情况。
5. 双击进行安装后，在右下角 ***托盘*** 处，你会看到如图图标。

![屏幕截图 2024-06-22 111326](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/8f54ca57-d8ba-4797-8396-ec07d2209e3c)
---
### 二、网络创建者（房主）的操作：
1. 回到 ***ZeroTier*** 官网：https://www.zerotier.com/
2. 选择 ***Sign Up*** 注册一个账号，然后 ***Log In*** 登录

![屏幕截图 2024-06-22 111740(1)(1)](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/0d609ccc-ad6a-4c2c-836c-bb1cfb410863)

3. ***Create A Network***，点击进一个 ***Network*** 中

![屏幕截图 2024-06-22 112057(1)(1)](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/942cfc68-5c69-4507-b936-fba6093f349d)

4. 复制 ***Network ID*** 给你的朋友

![屏幕截图 2024-06-22 112220](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/06ca82d4-b6e1-4fa3-8efe-879a00477c42)

5. 等待朋友发来请求，下拉找到请求，***勾选***

![屏幕截图 2024-06-22 112819](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/55b7a541-4feb-47a1-b85d-6b62872aef12)

6. 对此网络的管理均在此网页内进行
---
### 三、网络连接者：
1. 点击托盘图标，点击 ***Join New Network***

![屏幕截图 2024-06-22 112349(1)(1)](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/f2357b21-5092-4a28-83a8-7dcd874b7a1c)

2. 将代码输入，点击 ***Join***

![屏幕截图 2024-06-22 112555](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/6ad74f35-993c-4592-b44a-0c3786292741)

3. 等待创建者同意加入网络

![屏幕截图 2024-06-22 112920(1)(1)](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/c89f1641-671e-463e-94ad-3eb3c623bc06)
---
- ***注意*** : 请把 ***Windows防火墙*** 中的公用网络关闭，防止连接失败。
---
### 四、游戏房主：
1. 任意界面下按 ***win键*** + ***R键*** ，输入 ***cmd***

![屏幕截图 2024-06-22 113704](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/d2495ee4-b5cd-483f-97e2-24ebdbf750e8)

2. 输入 ***ipconfig*** 找到以太网Zerotier下的描述，复制 ***IPv4地址***

![屏幕截图 2024-06-22 113815](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/c86cb078-ca68-4e98-8031-dbeb8b3085c7)

3. 打开任意世界，***对局域网开放*** ，注意如果朋友是离线用户，一定要关闭 ***在线验证***

![屏幕截图 2024-06-22 113335](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/3bb916b0-a844-4eec-9bdf-9e47b62009cb)
![屏幕截图 2024-06-22 113441](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/5af288b8-349f-4aea-bb40-4ba50a68da75)

4. 将 ***端口号*** 和 ***IPv4地址*** 发给你的朋友
---
### 五、游戏玩家：
1. 多人游戏，添加服务器
2. 输入 ***IPv4地址*** ***:*** ***端口号*** ,注意 ***“:”*** 一定是英文输入法下的

![屏幕截图 2024-06-22 114134](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/89ea9d26-3733-466c-ad54-de552bcb4b8e)

3. 连接进入

![屏幕截图 2024-06-22 114410](https://github.com/RolinShmily/RolinShmily.github.io/assets/142618699/ae9dd8f4-d2f4-48cd-94e2-4ca93a75ac4c)
---
- 大功告成，如果遇到问题请提交 ***comment(评论)***，看到后会有更新。