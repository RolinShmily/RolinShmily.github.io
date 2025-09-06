---
title: CS2指令与配置
categories:
  - - Game
    - CS2
tags:
  - CS2
  - cfg
  - 游戏设置
  - 游戏指令
cover: >-
  https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/%E5%BE%AE%E4%BF%A1%E5%9B%BE%E7%89%87_20240913084859.jpg
abbrlink: b445fd38
date: 2025-04-12 00:00:00
updated: 2025-08-17 00:00:00
description:
keywords:
---
# 什么是 CFG

**cfg** 是 config(设置)的简写，可以理解为，拥有了 cfg，你就拥有了在任何地点快速开一把 cs 的能力，不用再为设置而担忧。

## CFG 存放位置

游戏全局 cfg：

- 如果你的游戏存放盘符与 steam 存放盘符不同，就参考前者，若相同，则后者。

**...\SteamLibrary\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg** 或 **...\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg**

- 当然也可以在 steam 程序中寻找，下面是步骤。

1. 打开 steam 库，找到 Counter-Strike 2，右击选择属性

![steam](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-12-52.webp)

2. 选择“已安装文件”，点击浏览

![steam2](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-14-48.webp)

3. 进入“game”，进入“csgo”，选择“cfg”，该目录下就是存放 cfg 文件的位置

![1](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-16-27.webp)

![2](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-18-32.webp)

![3](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-19-00.webp)

个人用户 cfg：
**...\Steam\userdata\123456789\730\local\cfg**

- 此处的“123456789”为 steamID，可用于添加好友，如果你的 PC 上有多个 steam 账号登录过，那么在 userdata 文件夹中你会看到多个用户文件夹。
- 与游戏全局 cfg 不同，个人用户 cfg 的设置只用于该 steam 账号，并且多了一个 **cs2_video.txt** 配置文件,我倾向于只用这个 video 配置来同步画面设置，而绑定键位等用全局 cfg。

## 如何创建一个 cfg 文件

1. 在桌面新建一个文本文档(也就是 txt)，可以直接在这个 txt 文件中编写配置

![1](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-38-17.webp)

2. 编写完成后，在文件资源管理器中找到这个文件，更改后缀为 cfg。

- 如果你无法显示后缀，按照下面操作

![2](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-41-02.webp)

## 备份与还原

- 控制台输入 `host_writeconfig backup` 可生成 `backup.cfg` 必要时在控制台输入 `exec backup` 即可恢复原设置
- 控制台输入 `binddefaults`后，将绑定默认按键，输入`key_listboundkeys` 可在控制台输出里查看所有默认按键绑定
## autoexec.cfg (模板)

这是一个只要你游戏启动就会自动加载的 cfg，所以基础设置与按键绑定，可以直接写在这个 cfg 文件里。

- 下面给出一个模板，改写完成后要将文件名改为“autoexec.cfg”，并放在游戏全局 cfg 存放位置，才能生效。

```ini
//键位
bind "w" "+forward" //前进
bind "s" "+back" //后退
bind "a" "+left" //向左
bind "d" "+right" //向右
bind "mouse1" "+attack" //左键攻击
bind "mouse2" "+attack2" //右键特殊攻击
bind "e" "+use" //使用
bind "f" "+lookatweapon" //检视
bind "space" "+jump"  //跳跃
bind "ctrl" "+duck"  //蹲下
bind "tab" "+showscores" //打开计分板
bind "g" "drop"   //丢弃装备
bind "m" "teammenu" //选择队伍
bind "shift" "+sprint" //静步
bind "b" "buymenu" //购买菜单
bind "z" "slot6" //雷
bind "x" "slot7" //闪
bind "c" "slot8" //烟
bind "6" "slot9" //诱饵弹
bind "v" "slot10" //火
bind "y" "+spray_menu" //打开涂鸦菜单
bind "i" "messagemode2"//团队聊天框
bind "u" "messagemode"//全局聊天框
bind "mouse4" "+voicerecord"//打开麦克风
bind "mouse5" "player_ping"//玩家示意标志
bind "mwheeldown" "+jump" //滚轮下跳
bind "mwheelup" "+jump"//滚轮上跳
bind "`" "toggleconsole"//打开控制台
bind "t" "switchhands"//切换左右手持枪
bind "h" "toggleradarscale" //切换小地图缩放
bind "ralt" "radio2;slot12" //无线电与X光

//准星
cl_crosshair_drawoutline "0" // 禁用十字准星的轮廓线
cl_crosshair_dynamic_maxdist_splitratio "1" // 动态十字准星的最大分离距离比例
cl_crosshair_dynamic_splitalpha_innermod "0" // 动态十字准星内部分离部分的透明度
cl_crosshair_dynamic_splitalpha_outermod "1" // 动态十字准星外部分离部分的透明度
cl_crosshair_dynamic_splitdist "3" // 动态十字准星的分离距离
cl_crosshair_friendly_warning "0" // 禁用对友军的十字准星警告
cl_crosshair_outlinethickness "1" // 十字准星轮廓线的厚度
cl_crosshair_sniper_show_normal_inaccuracy "0" // 禁用狙击枪十字准星显示正常不准确度
cl_crosshair_t "0" // 禁用T形十字准星
cl_crosshairalpha "255" // 十字准星的透明度（255为完全不透明）
cl_crosshaircolor 5 // 设置十字准星颜色为自定义（5表示自定义颜色）
cl_crosshaircolor_b "255" // 自定义十字准星的蓝色分量（255为最大）
cl_crosshaircolor_g "255" // 自定义十字准星的绿色分量（255为最大）
cl_crosshaircolor_r "0" // 自定义十字准星的红色分量（0为最小）
cl_crosshairdot "0" // 禁用十字准星中心点
cl_crosshairgap "-3.644676" // 设置十字准星的间隙（负值表示向内收缩）
cl_crosshairgap_useweaponvalue "0" // 禁用根据武器值调整十字准星间隙
cl_crosshairsize "0.901125" // 设置十字准星的大小
cl_crosshairstyle "4" // 设置十字准星样式为经典静态（4表示经典静态）
cl_crosshairthickness "0.961664" // 设置十字准星的厚度
cl_crosshairusealpha "1" // 启用十字准星的透明度设置

//狙击枪瞄准线宽度
cl_crosshair_sniper_width "2"

//鼠标灵敏度
sensitivity 0.50

//持枪视角
viewmodel_fov 68 // 设置第一人称视角的视野范围（FOV），值越大，视野越广
Viewmodel_offset_x 2.5 // 调整武器模型在水平方向（X轴）上的偏移，正值向右，负值向左
Viewmodel_offset_y 0 // 调整武器模型在垂直方向（Y轴）上的偏移，正值向上，负值向下
Viewmodel_offset_z -1.5 // 调整武器模型在深度方向（Z轴）上的偏移，正值向前，负值向后
viewmodel_presetpos 2 // 使用预设的武器模型位置（2表示经典位置）

//雷达
cl_radar_always_centered "0" // 禁用雷达始终以玩家为中心，雷达会显示地图的完整区域
cl_radar_scale "0.37" // 设置雷达的缩放比例，值越小，雷达显示的范围越大
cl_hud_radar_scale "1" // 设置HUD上雷达的缩放比例，1为默认大小
cl_teammate_colors_show 2 // 设置队友颜色显示模式，2表示显示队友的轮廓颜色
```

## cs2_video.txt (模板)

同步画面设置

- 给出模板

```ini
"video.cfg"
{
	"Version"		"15" // 配置文件版本号
	"VendorID"		"4318" // 显卡厂商 ID（例如 NVIDIA、AMD）
	"DeviceID"		"10464" // 显卡设备 ID
	"setting.cpu_level"		"3" // CPU 性能等级（0-3，3 为最高）
	"setting.gpu_mem_level"		"3" // GPU 显存性能等级（0-3，3 为最高）
	"setting.gpu_level"		"3" // GPU 性能等级（0-3，3 为最高）
	"setting.knowndevice"		"0" // 是否识别为已知设备（0 为否，1 为是）
	"setting.defaultres"		"1920" // 默认分辨率宽度（1920x1080）
	"setting.defaultresheight"		"1080" // 默认分辨率高度（1920x1080）
	"setting.refreshrate_numerator"		"0" // 刷新率分子（0 表示使用默认值）
	"setting.refreshrate_denominator"		"0" // 刷新率分母（0 表示使用默认值）
	"setting.fullscreen"		"1" // 是否启用全屏模式（0 为否，1 为是）
	"setting.coop_fullscreen"		"1" // 合作模式是否启用全屏（1 为是）
	"setting.nowindowborder"		"1" // 是否启用无边框窗口模式（1 为是）
	"setting.mat_vsync"		"0" // 是否启用垂直同步（0 为否，1 为是）
	"setting.fullscreen_min_on_focus_loss"		"0" // 失去焦点时是否最小化全屏窗口（0 为否）
	"setting.high_dpi"		"0" // 是否启用高 DPI 缩放（0 为否）
	"AutoConfig"		"2" // 自动配置等级（2 为自定义配置）
	"setting.shaderquality"		"0" // 着色器质量（0 为低，1 为中，2 为高）
	"setting.r_texturefilteringquality"		"3" // 纹理过滤质量（0-3，3 为最高）
	"setting.msaa_samples"		"4" // 多重采样抗锯齿（MSAA）采样数（4 为 4x MSAA）
	"setting.r_csgo_cmaa_enable"		"0" // 是否启用 CMAA 抗锯齿（0 为否）
	"setting.videocfg_shadow_quality"		"2" // 阴影质量（0 为低，1 为中，2 为高）
	"setting.videocfg_dynamic_shadows"		"1" // 是否启用动态阴影（1 为是）
	"setting.videocfg_texture_detail"		"2" // 纹理细节（0 为低，1 为中，2 为高）
	"setting.videocfg_particle_detail"		"2" // 粒子细节（0 为低，1 为中，2 为高）
	"setting.videocfg_ao_detail"		"2" // 环境光遮蔽（AO）细节（0 为低，1 为中，2 为高）
	"setting.videocfg_hdr_detail"		"3" // HDR 细节（0-3，3 为最高）
	"setting.videocfg_fsr_detail"		"0" // FSR（FidelityFX Super Resolution）细节（0 为禁用）
	"setting.monitor_index"		"0" // 显示器索引（0 为主显示器）
	"setting.r_low_latency"		"1" // 是否启用低延迟模式（1 为是）
	"setting.aspectratiomode"		"0" // 宽高比模式（0 为自动，1 为 4:3，2 为 16:9）
}
```

# 设置启动项

- 启动项设置位置：在 steam 库中选择 CS2 属性，选择“通用”，在下方黑框内填写。

![qidong](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-13_00-11-22.webp)

- 下面使一些常用启动项，需要注意的是，每一条指令之间要有一个空格。

```ini
-novid  //关闭过场动画,CS2中已失效
-high  //提高CSGO程序优先级，有可能负优化
-nojoy //关闭手柄相关，降低内存占用
-perfectworld  //直接进入国服
-worldwide  //直接进入国际服
-w 1920 -h 1080  //设置分辨率1920x1080
-noborder //无边框窗口化
+exec auto.cfg  //加载auto.cfg
+fps_max 300  //限制fps最大300
-allow_third_party_software  //允许OBS等第三方软件
-noreflex //取消游戏内的reflex功能，可以在NVIDIA控制面板中开启
```

# 控制台指令

了解控制台指令功能，可以将其绑定在按键上，并写入 cfg 文件，快速实现功能。

- 下面给出亿些指令

```ini
sv_cheats 1 // 开启作弊模式，允许使用作弊命令
bot_kick // 踢出所有机器人
mp_buy_anywhere 1 // 允许在任意位置购买装备
mp_freezetime 0 // 设置赛前准备时间为0秒
mp_maxmoney 99999 // 设置最大金钱数为99999
mp_startmoney 99999 // 设置起始金钱数为99999
mp_buytime 99999 // 设置购买时间为99999秒
mp_ignore_round_win_conditions 1 // 回合永不结束
mp_respawn_on_death_ct 1 // CT阵营无限复活
mp_respawn_on_death_t 1 // T阵营无限复活
mp_friendlyfire 1 // 开启队友伤害
ammo_grenade_limit_total 6 // 设置手榴弹最大可携带数为6
mp_spectators_max 9 // 设置游戏观察者最大数为9
mp_autokick 0 // 禁用自动踢出服务器功能
mp_restartgame 1 // 在1秒后重启回合
sv_grenade_trajectory_prac_pipreview 1 // 启用手榴弹轨迹的预览
sv_grenade_trajectory_prac_trailtime 8 // 设置手榴弹轨迹可见时间为8秒
sv_infinite_ammo 2 // 设置无限弹药模式（道具无限），但仍需换弹夹
sv_showimpacts 1 // 开启弹痕显示

exec autoexec.cfg // 执行 autoexec.cfg 配置文件，加载自定义设置
key_listboundkeys // 列出所有已绑定的按键及其对应的命令
toggle cl_teamid_overhead_mode 1 3 // 切换队友头顶标识模式（1 为简单标识，3 为详细标识）
toggle cl_draw_only_deathnotices 1 0 // 切换是否仅显示死亡通知（1 为仅显示，0 为显示完整 HUD）
toggle cl_drawhud_force_radar 1 0 // 切换是否强制显示雷达（1 为强制显示，0 为正常显示）

cl_hud_color "11" // 设置 HUD 颜色为粉色
con_enable "1" // 启用控制台功能
fps_max 0 // 设置 FPS 无上限，允许游戏以最高帧率运行
cl_join_advertise "2" // 显示玩家计划加入反恐精英队的信息
cl_use_opens_buy_menu "0" // 禁用在靠近购买区域时按下使用键（E键）自动打开购买菜单的功能
cl_dm_buyrandomweapons 0 // 在死亡竞技模式中禁用自动购买随机武器
gameinstructor_enable "0" // 禁用游戏指导功能
cl_autohelp "false" // 禁用自动帮助提示
mm_dedicated_search_maxping "70" // 优先选择延迟在 70 毫秒以内的服务器
func_break_max_pieces 0 // 游戏会根据物体的属性生成默认数量的碎片
r_drawtracers_firstperson 1 // 开启第一人称视角中的子弹轨迹显示
r_fullscreen_gamma 3.0 // 调整游戏画面伽马值为 3.0
cl_teamid_overhead_mode 3 // 始终显示队友名称与装备信息
echo AutoConfig Enabled! // 在控制台打印 "AutoConfig Enabled!" 提示信息

mp_damage_headshot_only 1 // 仅爆头才能造成伤害，其他部位攻击无效
ent_create chicken // 在游戏中生成一只鸡（娱乐功能）
custom_bot_difficulty 5 // 设置自定义 BOT 难度为最高（5 为最高难度）
mp_plant_c4_anywhere 1 // 允许在任何位置安放 C4 炸弹
mp_c4timer 40 // 设置 C4 炸弹的倒计时为 40 秒
sv_regeneration_force_on 1 // 开启生命值自动回复功能
cl_showpos 1 // 在屏幕上显示玩家当前的位置、速度和角度信息
mp_weapons_glow_on_ground 1 // 开启地面武器的高亮显示功能
```

# 如何查找及时映射的cfg代码参数
> 如果我们使用cfg来配置准星，是需要知道具体参数的，而CS提供的准星代码需要进游戏中导入，为了一键式配置，可参考以下方法，找到喜欢的准星导入后，在文件中找到准星具体参数复制。
- 找到如下路径 **...\Steam\userdata\123456789\730\local\cfg** ,找到如下文件打开。
![](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250420121101.png)
- 这里的参数就是准星参数
![](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250420121153.png)
> 查看所有刚刚更改的按键绑定，应对不知键位名称的情况。
- 下面这个文件里就是所有的按键绑定
![](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/PixPin_2025-07-25_03-18-22.png)
> 游戏的功能性设置，所对应的cfg代码参数，也有对应文件。以chatwheel轮盘配置为例说明。

- 首先打开下面这个文件
![](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/PixPin_2025-07-25_03-20-46.png)
- 下面的就是快捷轮盘对应槽位的关键词配置
![](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250721newstart/PixPin_2025-07-25_03-23-37.png)
# 自用配置分享
 

<button id="downloadBtn" onclick="packAndDownload()" style="padding: 8px 16px; background: #007bff; color: white; border: none; border-radius: 4px; cursor: pointer; display: inline-flex; align-items: center; gap: 8px;">
  <span>打包并打包下载全部CFG文件</span>
  <div id="loader" style="display: none; width: 16px; height: 16px; border: 2px solid rgba(255,255,255,0.3); border-radius: 50%; border-top-color: white; animation: spin 1s ease-in-out infinite;"></div>
</button>
<div id="statusMessage" style="margin-top: 8px; color: #666; font-size: 14px; height: 20px;"></div>

<style>
  @keyframes spin {
    to { transform: rotate(360deg); }
  }
</style>

<script src="https://cdn.jsdelivr.net/npm/jszip@3.10.1/dist/jszip.min.js"></script>
<script>
async function packAndDownload() {
  const btn = document.getElementById('downloadBtn');
  const loader = document.getElementById('loader');
  const statusMsg = document.getElementById('statusMessage');
  
  // 1. 准备阶段 - 更新UI状态
  btn.disabled = true;
  btn.style.background = '#6c757d';
  loader.style.display = 'block';
  statusMsg.textContent = '正在准备文件...';
  
  // 2. 定义文件列表
  const filesToPack = [
    { name: "autoexec.cfg", url: "./cfgs/autoexec.cfg" },
    { name: "crosshair_view.cfg", url: "./cfgs/crosshair_view.cfg" },
    { name: "demo.cfg", url: "./cfgs/demo.cfg" },
    { name: "hlae.cfg", url: "./cfgs/hlae.cfg" },
    { name: "knife.cfg", url: "./cfgs/knife.cfg" },
    { name: "lastinv.cfg", url: "./cfgs/lastinv.cfg" },
    { name: "train.cfg", url: "./cfgs/train.cfg" },
    { name: "zeus.cfg", url: "./cfgs/zeus.cfg" },
    { name: "spawn/ancient.cfg", url: "./cfgs/spawn/ancient.cfg" },
    { name: "spawn/anubis.cfg", url: "./cfgs/spawn/anubis.cfg" },
    { name: "spawn/dust2.cfg", url: "./cfgs/spawn/dust2.cfg" },
    { name: "spawn/inferno.cfg", url: "./cfgs/spawn/inferno.cfg" },
    { name: "spawn/init_spawns.cfg", url: "./cfgs/spawn/init_spawns.cfg" },
    { name: "spawn/italy.cfg", url: "./cfgs/spawn/italy.cfg" },
    { name: "spawn/mirage.cfg", url: "./cfgs/spawn/mirage.cfg" },
    { name: "spawn/nuke.cfg", url: "./cfgs/spawn/nuke.cfg" },
    { name: "spawn/office.cfg", url: "./cfgs/spawn/office.cfg" },
    { name: "spawn/spawn.cfg", url: "./cfgs/spawn/spawn.cfg" },
    { name: "spawn/vertigo.cfg", url: "./cfgs/spawn/vertigo.cfg" },
    { name: "crosshair_library/01.cfg", url: "./cfgs/crosshair_library/01.cfg" },
    { name: "crosshair_library/02.cfg", url: "./cfgs/crosshair_library/02.cfg" },
    { name: "crosshair_library/03.cfg", url: "./cfgs/crosshair_library/03.cfg" },
    { name: "crosshair_library/04.cfg", url: "./cfgs/crosshair_library/04.cfg" }
  ];

  // 3. 创建ZIP实例
  const zip = new JSZip();
  
  try {
    // 4. 循环下载文件并显示进度
    for (let i = 0; i < filesToPack.length; i++) {
      const file = filesToPack[i];
      // 更新进度信息
      statusMsg.textContent = `正在处理文件 ${i+1}/${filesToPack.length}: ${file.name}`;
      
      const response = await fetch(file.url);
      if (!response.ok) {
        throw new Error(`无法获取文件: ${file.name}`);
      }
      const content = await response.text();
      zip.file(file.name, content);
    }

    // 5. 生成ZIP并下载
    statusMsg.textContent = '正在生成压缩文件...';
    zip.generateAsync({ type: "blob" })
      .then(function(content) {
        const a = document.createElement("a");
        a.href = URL.createObjectURL(content);
        a.download = "Allcfgs.zip";
        document.body.appendChild(a);
        a.click();
        document.body.removeChild(a);
        URL.revokeObjectURL(a.href);
        
        // 下载完成
        statusMsg.textContent = '下载完成!';
      });

  } catch (error) {
    console.error("打包失败:", error);
    statusMsg.textContent = `错误: ${error.message}`;
    statusMsg.style.color = '#dc3545';
  } finally {
    // 恢复按钮状态
    setTimeout(() => {
      btn.disabled = false;
      btn.style.background = '#28a745';
      loader.style.display = 'none';
      
      // 5秒后清除状态消息
      if (statusMsg.textContent !== '错误: 无法获取文件') {
        setTimeout(() => statusMsg.textContent = '', 5000);
      }
    }, 1000);
  }
}
</script>

[云盘存储地址](https://openlist.srprolin.top/blog/CS2-CFGS/cfgs)

- 下载可能会有延迟，请耐心等待，并且请注意浏览器拦截下载。 
- 下载完成后会得到一个压缩包`Allcfgs.zip`，直接放进cfg文件夹，并右击选择“解压到此文件夹“即可。

## 启动项

```ini
-allow_third_party_software -noreflex -high -novid -nojoy -noborder -worldwide
```

## cs2_video.txt
- `视频配置文件`：<a href="./video_config/cs2_video.txt" class="file-link" data-filename="cs2_video.txt">cs2_video.txt</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
-  集合了“高级视频选项”、“分辨率”、“显示模式”
## autoexec.cfg
- `自启动Config`：<a href="./cfgs/autoexec.cfg" class="file-link" data-filename="autoexec.cfg">autoexec.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 注意查看控制台导航信息。
## train.cfg
- `跑图Config`：<a href="./cfgs/train.cfg" class="file-link" data-filename="train.cfg">train.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 注意查看控制台导航信息。
- “p”键启用，出生点预设参考于 **Bad0RANG3** ，项目地址：https://github.com/Bad0RANG3/CS2PraticeCFG ，个人空间：https://space.bilibili.com/482966540

> 注意以下 cfg 都需要存放在游戏全局 cfg 文件夹下的 spawn 文件夹内，比如 **...\SteamLibrary\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\spawn** 或 **...\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\spawn** 下。

### spawn.cfg
- `重生点控制台Config`：<a href="./cfgs/spawn/spawn.cfg" class="file-link" data-filename="spawn.cfg">spawn.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）

### vertigo.cfg
- `vertigo重生点Config`：<a href="./cfgs/spawn/vertigo.cfg" class="file-link" data-filename="vertigo.cfg">vertigo.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）

### office.cfg
- `office重生点Config`：<a href="./cfgs/spawn/office.cfg" class="file-link" data-filename="office.cfg">office.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）

### nuke.cfg
- `nuke重生点Config`：<a href="./cfgs/spawn/nuke.cfg" class="file-link" data-filename="nuke.cfg">nuke.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）

### mirage.cfg
- `mirage重生点Config`：<a href="./cfgs/spawn/mirage.cfg" class="file-link" data-filename="mirage.cfg">mirage.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）

### italy.cfg
- `italy重生点Config`：<a href="./cfgs/spawn/italy.cfg" class="file-link" data-filename="italy.cfg">italy.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
### inferno.cfg
- `inferno重生点Config`：<a href="./cfgs/spawn/inferno.cfg" class="file-link" data-filename="inferno.cfg">inferno.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
### dust2.cfg
- `dust2重生点Config`：<a href="./cfgs/spawn/dust2.cfg" class="file-link" data-filename="dust2.cfg">dust2.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
### anubis.cfg
- `anubis重生点Config`：<a href="./cfgs/spawn/anubis.cfg" class="file-link" data-filename="anubis.cfg">anubis.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）

### ancient.cfg
- `ancient重生点Config`：<a href="./cfgs/spawn/ancient.cfg" class="file-link" data-filename="ancient.cfg">ancient.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
### init_spawns.cfg
- `重生点初始化Config`：<a href="./cfgs/spawn/init_spawns.cfg" class="file-link" data-filename="init_spawns.cfg">init_spawns.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）

---

## demo.cfg
- `看demo专用Config`：<a href="./cfgs/demo.cfg" class="file-link" data-filename="demo.cfg">demo.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 集成了一些实用指令的快捷键
- 取自 Purp1e 老师：https://space.bilibili.com/73115492
- 注意查看控制台导航信息。
## hlae.cfg
- `HLAE观赛Config`：<a href="./cfgs/hlae.cfg" class="file-link" data-filename="hlae.cfg">hlae.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 集成了一些HLAE的实用指令的快捷键
- 同样取自 Purp1e 老师：https://space.bilibili.com/73115492
- 注意查看控制台导航信息。
## knife.cfg
- `匕首模型更换Config`：<a href="./cfgs/knife.cfg" class="file-link" data-filename="knife.cfg">knife.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 注意控制台导航信息
- “j”键启用，命令完成后有聊天框提示

## lastinv.cfg
> 2025.8.15更新：此cfg已不再适用，Valve在更新中使切装备动画在衔接检视时的延迟变为0，此cfg效果可以由在切换装备前按住“检视键”来实现。
- `切刀自动检视Config`：<a href="./cfgs/lastinv.cfg" class="file-link" data-filename="lastinv.cfg">lastinv.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- “弯刀”专用，规避了切刀时的双手拔刀动作，而是直接检视
- 注意该配置重写了Q键(更换为最近装备)、1键(主武器)、2键(副武器)、3键(匕首刀)的逻辑，请不要修改这4个按键的默认功能。
- “/”键启用，启用后“.”键取消该设置，与弯刀搭配使用，避免了切刀时的双手动作。

## zeus.cfg
- `电击枪即用即切Config`：<a href="./cfgs/zeus.cfg" class="file-link" data-filename="zeus.cfg">zeus.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 电击枪快捷切换
- 在 autoexec.cfg 中自动启用，必须绑定“4”键电击枪，在电击枪左键使用之后自动切出主武器/副武器，手持电击枪右键时则不使用，直接切出主武器/副武器。
- Tips: 电击枪充电完成是有声音的，请注意使用后利用该声音做一定战术调整，或者直接将其丢弃，避免在关键时刻暴露位置。
## crosshair_view.cfg
- `准星与持枪视角库Config`：<a href="./cfgs/crosshair_view.cfg" class="file-link" data-filename="crosshair_view.cfg">crosshair_view.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 准星与持枪视角的存储与即时更换
- 若更换准星必须搭配crosshair_library准星代码库使用
- "["键启用，注意查看控制台导航信息。
- Tips: 如果你有能力，可以自己根据代码魔改，将源代码绑定按键，实现一键切换准星/持枪视角。
> 由于Valve的脚本指令单条有长度限制，而准星参数的设置已经超过该限制，故直接用cfg文件来保存准星预设。
> 注意以下 cfg 都需要存放在游戏全局 cfg 文件夹下的 crosshair_library 文件夹内，比如 **...\SteamLibrary\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\crosshair_library** 或 **...\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\crosshair_library** 下。
### crosshair_library
> 这里仅给出库中的准星代码、源码以及持枪视角源码，后续将会以GIF格式在此展示准星与持枪视角。
- `01号准星Config`：<a href="./cfgs/crosshair_library/01.cfg" class="file-link" data-filename="01.cfg">01.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 准星代码: `CSGO-H9mcs-8GDFZ-MfxkQ-2Kx7O-pTLoD`

- `02号准星Config`：<a href="./cfgs/crosshair_library/02.cfg" class="file-link" data-filename="02.cfg">02.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 准星代码: `CSGO-oK2db-LY2wT-seq73-YTnJB-3bOUD`

- `03号准星Config`：<a href="./cfgs/crosshair_library/03.cfg" class="file-link" data-filename="03.cfg">03.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 准星代码: `CSGO-9StUb-FrcBs-HhYjr-mzVip-YScNE`

- `04号准星Config`：<a href="./cfgs/crosshair_library/04.cfg" class="file-link" data-filename="04.cfg">04.cfg</a>
- - 单击`(Click)`查看文件，`Ctrl+单击(click)`下载文件。（请注意浏览器拦截下载）
- 准星代码: `CSGO-pqEaF-5AKXB-DCdnh-vpxAJ-94GSQ`

---
# lulu's cfg
- 修改了autoexec的默认按键绑定与crosshair_view的内容
- 点击`云盘存储地址`查看并下载所更改文件
- 可以先下载`全部自用配置cfg`,再下载此部分,将修改后的内容覆盖原来的文件.
[云盘存储地址](https://openlist.srprolin.top/blog/CS2-CFGS/lulu)


<button id="downloadBtn" onclick="packAndDownloadLulu()" style="padding: 8px 16px; background: #28a745; color: white; border: none; border-radius: 4px; cursor: pointer; display: inline-flex; align-items: center; gap: 8px;">
  <span>打包并下载全部CFG文件(此链接为全部cfg)</span>
  <div id="loader" style="display: none; width: 16px; height: 16px; border: 2px solid rgba(255,255,255,0.3); border-radius: 50%; border-top-color: white; animation: spin 1s ease-in-out infinite;"></div>
</button>
<div id="statusMessage" style="margin-top: 8px; color: #666; font-size: 14px; height: 20px;"></div>

<style>
  @keyframes spin {
    to { transform: rotate(360deg); }
  }
</style>

<script src="https://cdn.jsdelivr.net/npm/jszip@3.10.1/dist/jszip.min.js"></script>
<script>
async function packAndDownloadLulu() {
  const btn = document.getElementById('downloadBtn');
  const loader = document.getElementById('loader');
  const statusMsg = document.getElementById('statusMessage');
  
  // 1. 准备阶段 - 更新UI状态
  btn.disabled = true;
  btn.style.background = '#6c757d';
  loader.style.display = 'block';
  statusMsg.textContent = '正在准备文件...';
  
  // 2. 定义文件列表
  const filesToPack = [
    { name: "autoexec.cfg", url: "./lulu/autoexec.cfg" },
    { name: "crosshair_view.cfg", url: "./lulu/crosshair_view.cfg" },
    { name: "demo.cfg", url: "./cfgs/demo.cfg" },
    { name: "hlae.cfg", url: "./cfgs/hlae.cfg" },
    { name: "knife.cfg", url: "./cfgs/knife.cfg" },
    { name: "lastinv.cfg", url: "./cfgs/lastinv.cfg" },
    { name: "train.cfg", url: "./cfgs/train.cfg" },
    { name: "zeus.cfg", url: "./cfgs/zeus.cfg" },
    { name: "spawn/ancient.cfg", url: "./cfgs/spawn/ancient.cfg" },
    { name: "spawn/anubis.cfg", url: "./cfgs/spawn/anubis.cfg" },
    { name: "spawn/dust2.cfg", url: "./cfgs/spawn/dust2.cfg" },
    { name: "spawn/inferno.cfg", url: "./cfgs/spawn/inferno.cfg" },
    { name: "spawn/init_spawns.cfg", url: "./cfgs/spawn/init_spawns.cfg" },
    { name: "spawn/italy.cfg", url: "./cfgs/spawn/italy.cfg" },
    { name: "spawn/mirage.cfg", url: "./cfgs/spawn/mirage.cfg" },
    { name: "spawn/nuke.cfg", url: "./cfgs/spawn/nuke.cfg" },
    { name: "spawn/office.cfg", url: "./cfgs/spawn/office.cfg" },
    { name: "spawn/spawn.cfg", url: "./cfgs/spawn/spawn.cfg" },
    { name: "spawn/vertigo.cfg", url: "./cfgs/spawn/vertigo.cfg" },
    { name: "crosshair_library/01.cfg", url: "./cfgs/crosshair_library/01.cfg" },
    { name: "crosshair_library/02.cfg", url: "./cfgs/crosshair_library/02.cfg" },
    { name: "crosshair_library/03.cfg", url: "./cfgs/crosshair_library/03.cfg" },
    { name: "crosshair_library/04.cfg", url: "./cfgs/crosshair_library/04.cfg" }
  ];

  // 3. 创建ZIP实例
  const zip = new JSZip();
  
  try {
    // 4. 循环下载文件并显示进度
    for (let i = 0; i < filesToPack.length; i++) {
      const file = filesToPack[i];
      // 更新进度信息
      statusMsg.textContent = `正在处理文件 ${i+1}/${filesToPack.length}: ${file.name}`;
      
      const response = await fetch(file.url);
      if (!response.ok) {
        throw new Error(`无法获取文件: ${file.name}`);
      }
      const content = await response.text();
      zip.file(file.name, content);
    }

    // 5. 生成ZIP并下载
    statusMsg.textContent = '正在生成压缩文件...';
    zip.generateAsync({ type: "blob" })
      .then(function(content) {
        const a = document.createElement("a");
        a.href = URL.createObjectURL(content);
        a.download = "AllcfgsForLulu.zip";
        document.body.appendChild(a);
        a.click();
        document.body.removeChild(a);
        URL.revokeObjectURL(a.href);
        
        // 下载完成
        statusMsg.textContent = '下载完成!';
      });

  } catch (error) {
    console.error("打包失败:", error);
    statusMsg.textContent = `错误: ${error.message}`;
    statusMsg.style.color = '#dc3545';
  } finally {
    // 恢复按钮状态
    setTimeout(() => {
      btn.disabled = false;
      btn.style.background = '#28a745';
      loader.style.display = 'none';
      
      // 5秒后清除状态消息
      if (statusMsg.textContent !== '错误: 无法获取文件') {
        setTimeout(() => statusMsg.textContent = '', 5000);
      }
    }, 1000);
  }
}
</script>

- 下载可能会有延迟，请耐心等待，并且请注意浏览器拦截下载。    
- 下载完成后会得到一个压缩包，直接放进cfg文件夹，并右击选择“解压到此文件夹“即可。

<!--  预览样式：用于美化预览区域 -->
<style>
  .cfg-preview-modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0,0,0,0.7);
    z-index: 1000;
    padding: 2rem;
    box-sizing: border-box;
  }
  .cfg-preview-content {
    background: white;
    width: 100%;
    max-width: 800px;
    height: 80vh;
    margin: 0 auto;
    padding: 1.5rem;
    border-radius: 8px;
    overflow: auto;
    position: relative;
  }
  .cfg-close-btn {
    position: absolute;
    top: 1rem;
    right: 1rem;
    background: #ff4444;
    color: white;
    border: none;
    width: 30px;
    height: 30px;
    border-radius: 50%;
    cursor: pointer;
  }
  .cfg-download-btn {
    margin-top: 1rem;
    padding: 0.5rem 1rem;
    background: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  .cfg-file-content {
    white-space: pre; /* 保留文本中的空格和换行 */
    font-family: monospace; /* 使用等宽字体，适合代码/配置文件 */
    color: #333;
  }
  /* 深色主题样式 - 基于data-theme="dark" */
  html[data-theme="dark"] .cfg-preview-content {
    background: #1e1e1e; /* 深色背景 */
  }
  html[data-theme="dark"] .cfg-file-content {
    color: #e0e0e0; /* 浅色文本 */
  }
  html[data-theme="dark"] .cfg-close-btn {
    background: #d12525; /* 深色主题下的关闭按钮颜色 */
  }
  html[data-theme="dark"] .cfg-download-btn {
    background: #0b5ed7; /* 深色主题下的下载按钮颜色 */
  }
</style>

<!-- 预览模态框（默认隐藏） -->
<div class="cfg-preview-modal" id="cfgPreviewModal">
  <div class="cfg-preview-content">
    <button class="cfg-close-btn" onclick="closePreview()">×</button>
    <h3 id="previewFileName"></h3>
    <pre class="cfg-file-content" id="previewContent"></pre>
    <button class="cfg-download-btn" onclick="downloadCurrentFile()">下载此文件</button>
  </div>
</div>

<!-- 按键监听与文件预览脚本：区分单击和Ctrl+单击行为，单击显示预览 -->
<script>
  // 存储当前预览的文件信息
  let currentFileInfo = null;

  // 监听所有CFG链接的点击事件
  document.querySelectorAll('.file-link').forEach(link => {
    link.addEventListener('click', async (e) => {
      // 判断是否按下Ctrl/Command键（用于下载）
      const isCtrlPressed = e.ctrlKey || e.metaKey;
      
      if (isCtrlPressed) {
        // Ctrl+单击：直接下载
        e.preventDefault();
        const fileUrl = link.href;
        const fileName = link.dataset.filename;
        downloadFile(fileUrl, fileName);
      } else {
        // 普通单击：预览文件内容
        e.preventDefault();
        const fileUrl = link.href;
        const fileName = link.dataset.filename;
        
        try {
          // 获取文件内容
          const response = await fetch(fileUrl);
          if (!response.ok) throw new Error('文件不存在或无法访问');
          const content = await response.text();
          
          // 存储当前文件信息（用于下载按钮）
          currentFileInfo = { url: fileUrl, name: fileName };
          
          // 显示预览模态框
          document.getElementById('previewFileName').textContent = fileName;
          document.getElementById('previewContent').textContent = content;
          document.getElementById('cfgPreviewModal').style.display = 'block';
        } catch (error) {
          console.error('预览失败:', error);
          alert('无法预览文件：' + error.message);
        }
      }
    });
  });

  // 关闭预览模态框
  function closePreview() {
    document.getElementById('cfgPreviewModal').style.display = 'none';
    currentFileInfo = null;
  }

  // 下载当前预览的文件
  function downloadCurrentFile() {
    if (currentFileInfo) {
      downloadFile(currentFileInfo.url, currentFileInfo.name);
    }
  }

  // 通用下载函数
  function downloadFile(url, filename) {
    fetch(url)
      .then(response => response.blob())
      .then(blob => {
        const blobUrl = URL.createObjectURL(blob);
        const a = document.createElement('a');
        a.href = blobUrl;
        a.download = filename;
        a.click();
        setTimeout(() => URL.revokeObjectURL(blobUrl), 100);
      })
      .catch(error => {
        console.error('下载失败:', error);
        alert('下载失败，请重试');
      });
  }

  // 点击模态框外部关闭预览
  document.getElementById('cfgPreviewModal').addEventListener('click', (e) => {
    if (e.target === document.getElementById('cfgPreviewModal')) {
      closePreview();
    }
  });

  // 按ESC键关闭预览
  document.addEventListener('keydown', (e) => {
    if (e.key === 'Escape' && document.getElementById('cfgPreviewModal').style.display === 'block') {
      closePreview();
    }
  });
</script>