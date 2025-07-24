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
updated: 2025-07-14 00:00:00
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

# 如何查找准星代码与参数
> 如果我们使用cfg来配置准星，是需要知道具体参数的，而CS提供的准星代码需要进游戏中导入，为了一键式配置，可参考以下方法，找到喜欢的准星导入后，在文件中找到准星具体参数复制。
- 找到如下路径 **...\Steam\userdata\123456789\730\local\cfg** ,找到如下文件打开。

![](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250420121101.png)

- 这里的参数就是准星参数

![](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/20250420121153.png)

# 自用配置分享

## 启动项

```ini
-allow_third_party_software -noreflex -high -novid -nojoy -noborder -w 1440 -h 1080 -worldwide
```

## cs2_video.txt

```ini
"video.cfg"
{
	"Version"		"15"
	"VendorID"		"4318"
	"DeviceID"		"10464"
	"setting.cpu_level"		"3"
	"setting.gpu_mem_level"		"3"
	"setting.gpu_level"		"3"
	"setting.knowndevice"		"0"
	"setting.defaultres"		"1440"
	"setting.defaultresheight"		"1080"
	"setting.refreshrate_numerator"		"0"
	"setting.refreshrate_denominator"		"0"
	"setting.fullscreen"		"0"
	"setting.coop_fullscreen"		"1"
	"setting.nowindowborder"		"1"
	"setting.mat_vsync"		"0"
	"setting.fullscreen_min_on_focus_loss"		"0"
	"setting.high_dpi"		"0"
	"AutoConfig"		"2"
	"setting.shaderquality"		"0"
	"setting.r_texturefilteringquality"		"3"
	"setting.msaa_samples"		"4"
	"setting.r_csgo_cmaa_enable"		"0"
	"setting.videocfg_shadow_quality"		"1"
	"setting.videocfg_dynamic_shadows"		"1"
	"setting.videocfg_texture_detail"		"1"
	"setting.videocfg_particle_detail"		"1"
	"setting.videocfg_ao_detail"		"0"
	"setting.videocfg_hdr_detail"		"3"
	"setting.videocfg_fsr_detail"		"0"
	"setting.monitor_index"		"0"
	"setting.r_low_latency"		"1"
	"setting.aspectratiomode"		"0"
}
```

- 集合了“高级视频选项”、“分辨率”、“显示模式”

## autoexec.cfg

```ini
//Mouse
sensitivity 0.50                   // 灵敏度
zoom_sensitivity_ratio 1 		   // 开镜灵敏度
m_yaw 0.022                        // x轴速度
//Keys
bind "w" "+forward"                // 向前移动
bind "s" "+back"                   // 向后移动
bind "a" "+left"                   // 向左移动
bind "d" "+right"                  // 向右移动
bind "mouse1" "+attack"            // 普通攻击
bind "mouse2" "+attack2"           // 特殊攻击
bind "mouse_x" "yaw"               // 鼠标水平移动控制视角
bind "mouse_y" "pitch"             // 鼠标垂直移动控制视角
bind "e" "+use"                    // 使用/互动
bind "r" "+reload"                 // 装填弹药
bind "f" "+lookatweapon"           // 检视
bind "space" "+jump"               // 跳跃
bind "ctrl" "+duck"                // 蹲下
bind "tab" "+showscores"           // 显示计分板
bind "g" "drop"                    // 丢弃物品
bind "m" "teammenu"                // 打开队伍选择菜单
bind "shift" "+sprint"             // 静步
bind "b" "buymenu"                 // 打开购买菜单
bind "1" "slot1"                   // 主武器
bind "2" "slot2"                   // 副武器
bind "3" "slot3"                   // 匕首
bind "4" "slot11"                  // 电击枪
bind "5" "slot5"                   // C4
bind "z" "slot6;"                  // 雷
bind "x" "slot7"                   // 闪
bind "c" "slot8"                   // 烟
bind "6" "slot9"                   // 诱饵弹
bind "v" "slot10"                  // 火
bind "q" "lastinv"                 // 切换到上一个武器
bind "y" "+spray_menu"             // 打开喷漆菜单
bind "i" "messagemode2"            // 打开团队聊天
bind "u" "messagemode"             // 打开全局聊天
bind "mouse4" "+voicerecord"       // 语音
bind "alt" "+radialradio"          // 快捷聊天轮盘
bind "mouse5" "player_ping"		   // 玩家标记
bind "mwheeldown" "+jump"          // 鼠标滚轮向下跳跃
bind "mwheelup" "+jump"            // 鼠标滚轮向上跳跃
bind "`" "toggleconsole"                           // 打开/关闭控制台
bind "t" "switchhands"                             // 切换武器持握方式（左手/右手）
bind "h" "toggleradarscale"                        // 切换雷达缩放比例
bind "ralt" "toggle cl_teamid_overhead_mode 1 3"   // 切换队友头顶标识模式
bind "'" "radio2;slot12"                           // 打开无线电菜单、X光显示、医疗针
//bind "'" "+quickinv"							   // 轮盘切装备
bind "-" "toggle cl_draw_only_deathnotices 1 0"    // 切换是否仅显示死亡通知与准星
bind "=" "toggle cl_drawhud_force_radar 1 0"       // 切换是否强制显示雷达
bind F1 "vote 1"                                   // 投票选择同意
bind F2 "vote 2"                                   // 投票选择拒绝
bind "f5" "buy hegrenade"                          // 购买高爆手雷
bind "f6" "buy flashbang"                          // 购买闪光弹
bind "f7" "buy smokegrenade"                       // 购买烟雾弹
bind "f8" "buy molotov;buy incgrenade"             // 购买燃烧瓶/燃烧弹
bind "f9" "buy vest"                               // 购买防弹衣
bind "f10" "buy vesthelm"                          // 购买防弹衣+头盔
bind "f11" "buy defuser"                           // 购买拆弹器
bind "f4" "buy rifle1"                             // 购买主武器（步枪第二槽位）
bind "f3" "buy secondary4"                         // 购买副武器（手枪第五槽位）
bind "f12" "sellbackall"                           // 出售所有已购买物品
//cfg
exec zeus.cfg
bind "o" "exec crosshair_view;say_team crosshair_view!"
bind "\" "say_team keys_log!;echoln "CFG按键指示";echoln "- 自启动：zeus电击枪快速切换";echoln "- o：autoexec重启配置";echoln "- j：knife匕首模型轮换";echoln "- p：train跑图模式";echoln "- [：crosshair轮换准星设置";echoln "- ]：view轮换持枪视角";echoln "- /：lastinv弯刀检视优化";echoln "- k：一键发刀";echoln "- o：默认准星与视角""
bind "j" "exec knife.cfg;say_team knife_model!"
bind "p" "exec train.cfg;say_team train_model!"
bind "[" "exec crosshair_view;say_team crosshair_view!"
bind "]" "exec crosshair_view;say_team crosshair_view!"
bind "/" "exec lastinv.cfg;say_team lastinv!"
bind "k" "say_team !drop"
//准星
cl_crosshair_drawoutline "false"                     // 禁用准星轮廓绘制
cl_crosshair_dynamic_maxdist_splitratio "0.300000"   // 动态准星最大分离距离的比例
cl_crosshair_dynamic_splitalpha_innermod "1.000000"  // 动态准星内部分离部分的透明度
cl_crosshair_dynamic_splitalpha_outermod "0.500000"  // 动态准星外部分离部分的透明度
cl_crosshair_dynamic_splitdist "7"                   // 动态准星分离距离
cl_crosshair_outlinethickness "1.000000"             // 准星轮廓的厚度（如果启用轮廓）
cl_crosshair_recoil "false"                          // 禁用准星随武器后坐力动态变化
cl_crosshair_t "false"                               // 禁用T形准星
cl_crosshairalpha "255"                              // 准星的透明度（255为完全不透明）
cl_crosshaircolor "5"                                // 准星颜色（5为自定义颜色）
cl_crosshaircolor_b "255"                            // 准星颜色的蓝色分量（RGB）
cl_crosshaircolor_g "255"                            // 准星颜色的绿色分量（RGB）
cl_crosshaircolor_r "255"                            // 准星颜色的红色分量（RGB）
cl_crosshairdot "false"                              // 禁用准星中心点
cl_crosshairgap "-3.400000"                          // 准星间隙大小（负值表示准星向内收缩）
cl_crosshairgap_useweaponvalue "false"               // 禁用根据武器调整准星间隙
cl_crosshairsize "0.900000"                          // 准星大小
cl_crosshairstyle "4"                                // 准星样式（4为经典静态准星）
cl_crosshairthickness "0.800000"                     // 准星线条的厚度
cl_crosshairusealpha "true"                          // 启用准星透明度设置
cl_crosshair_sniper_width "2"						 // 狙击镜准星线粗细
//投掷物准星
cl_fixedcrosshaigap "3"                   // 设置固定准星的间隙大小
cl_grenadecrosshair_decoy 1               // 启用诱饵弹的投掷轨迹准星
cl_grenadecrosshair_explosive 1           // 启用爆炸物（如手雷）的投掷轨迹准星
cl_grenadecrosshair_fire 1                // 启用燃烧弹的投掷轨迹准星
cl_grenadecrosshair_flash 1               // 启用闪光弹的投掷轨迹准星
cl_grenadecrosshair_keepusercrosshair 1   // 投掷时保留玩家自定义准星
cl_grenadecrosshair_smoke 1               // 启用烟雾弹的投掷轨迹准星
cl_grenadecrosshairdelay_decoy "0.114345" // 设置诱饵弹投掷轨迹准星的延迟时间
cl_grenadecrosshairdelay_explosive "0.114345" // 设置爆炸物投掷轨迹准星的延迟时间
cl_grenadecrosshairdelay_fire "0.114345"  // 设置燃烧弹投掷轨迹准星的延迟时间
cl_grenadecrosshairdelay_flash "0.114345" // 设置闪光弹投掷轨迹准星的延迟时间
cl_grenadecrosshairdelay_smoke "0.114345" // 设置烟雾弹投掷轨迹准星的延迟时间
//其余准星设置
cl_observed_bot_crosshair 2               // 观察机器人时显示准星（2为始终显示）
cl_show_observer_crosshair 2              // 观察其他玩家时显示准星（2为始终显示）
cl_teamid_overhead_fade_near_crosshair "0.5" // 设置队友ID在准星附近时的淡出距离
//持枪视角
viewmodel_fov 68                  // 设置视角模型（武器）的视野范围
viewmodel_offset_x 2              // 调整视角模型在X轴上的偏移（左右位置）
viewmodel_offset_y 2              // 调整视角模型在Y轴上的偏移（前后位置）
viewmodel_offset_z -1             // 调整视角模型在Z轴上的偏移（上下位置）
viewmodel_presetpos 0             // 禁用预设的视角模型位置，允许自定义偏移
//雷达
cl_radar_always_centered "0"        // 雷达不居中，显示整个地图
cl_radar_scale "0.37"               // 设置雷达缩放比例为 0.37
cl_hud_radar_scale "1"              // 设置 HUD 雷达缩放比例为 1
cl_teammate_colors_show "2"         // 显示队友颜色为 2（默认颜色模式）
cl_radar_icon_scale_min "0.6"       // 设置雷达图标最小缩放比例为 0.6
cl_radar_rotate "1"                 // 雷达随玩家视角旋转
//网络
cl_hud_telemetry_frametime_show 2  // 显示帧生成时间及FPS
cl_hud_telemetry_ping_show 2       // 显示延迟
mm_dedicated_search_maxping "70"   // 设置匹配时允许的最大 ping 值
//功能
cl_prefer_lefthanded 0             // 右手持枪（默认）
cl_debounce_zoom 0                 // 按住开镜键持续切换
cl_silencer_mode 1                 // 开启卸下消音器
cl_use_opens_buy_menu "0"          // 关闭E键打开购买菜单
cl_dm_buyrandomweapons 0           // 关闭死斗随机买枪
cl_teamcounter_playercount_instead_of_avatars 1 // 显示对局存活数字
r_drawtracers_firstperson 1        // 显示曳光弹
r_fullscreen_gamma 2.6             // 设置亮度
cl_teamid_overhead_mode 3          // 隔墙显示队友位置
cl_teamid_overhead_colors_show 1   // 玩家ID上使用玩家颜色
//声音
volume 1                              // 主音量
snd_headphone_eq 0                    // 均衡器
snd_menumusic_volume 0.03             // 主菜单音乐音量
snd_roundstart_volume 0               // 回合开始音量
snd_roundend_volume 0.02              // 回合结束音量
snd_roundaction_volume 0              // 回合开始行动音量
snd_mvp_volume 0.12                   // MVP音量
snd_mapobjective_volume 0.12          // 炸弹/人质音量
snd_tensecondwarning_volume 0.08      // 十秒警告音量
snd_deathcamera_volume 0.08           // 死亡视角音量
snd_mute_mvp_music_live_players 1     // 当双方团队成员都存活时关闭 MVP 音乐
snd_mute_losefocus 0                  // 后台播放声音
voice_modenable 1                     // 启用语音
//HUD
hud_showtargetid "1"               // 显示队友/敌人的 ID
hud_scaling "0.85"                 // 设置 HUD 缩放比例
safezonex "0.88"                   // 设置 HUD 水平占比
safezoney "0.905"                  // 设置 HUD 竖直占比
cl_color "4"                       // 设置队伍中玩家颜色
cl_hud_color "11"                  // 设置 HUD 颜色
cl_showloadout "0"                 // 不总显示物品栏
//其他
con_enable "1"                     // 启用开发者控制台
fps_max 0                          // 帧率无上限
cl_join_advertise "2"              // 公开游戏会话
gameinstructor_enable "0"          // 禁用教学提示系统
cl_autohelp "false"                // 禁用自动帮助提示
func_break_max_pieces 0            // 可破坏物体破碎时最大碎片数
r_show_build_info 0                // 关闭版本信息
spec_replay_autostart 0            // 关闭被击杀回放
//Ending
echo AutoConfig Enabled!
```

- "\"键启用 cfg 按键指南，在控制台查看。

## 璐璐的cfg
- [点我下载](https://cdn.jsdelivr.net/gh/RolinShmily/RolinShmily.github.io@refs/heads/main/source/_posts/CS2-Config/%E7%92%90%E7%92%90cfg/autoexec.cfg) 下载完成后，直接放进cfg文件夹即可。
- 注意要把文件名改为`autoexec.cfg`，`.cfg`是后缀名。
```
//Mouse
sensitivity 1.25                   // 灵敏度
zoom_sensitivity_ratio 1 		   // 开镜灵敏度
m_yaw 0.022                        // x轴速度
//Keys
bind "w" "+forward"                // 向前移动
bind "s" "+back"                   // 向后移动
bind "a" "+left"                   // 向左移动
bind "d" "+right"                  // 向右移动
bind "mouse1" "+attack"            // 普通攻击
bind "mouse2" "+attack2"           // 特殊攻击
bind "mouse_x" "yaw"               // 鼠标水平移动控制视角
bind "mouse_y" "pitch"             // 鼠标垂直移动控制视角
bind "e" "+use"                    // 使用/互动
bind "r" "+reload"                 // 装填弹药
bind "f" "+lookatweapon"           // 检视
bind "space" "+jump"               // 跳跃
bind "mouse4" "+duck"                // 蹲下
bind "tab" "+showscores"           // 显示计分板
bind "g" "drop"                    // 丢弃物品
bind "m" "teammenu"                // 打开队伍选择菜单
bind "shift" "+sprint"             // 静步
bind "b" "buymenu"                 // 打开购买菜单
bind "1" "slot1"                   // 主武器
bind "2" "slot2"                   // 副武器
bind "3" "slot3"                   // 匕首
bind "4" "slot11"                  // 电击枪
bind "5" "slot5"                   // C4
bind "z" "slot6;"                  // 雷
bind "q" "slot7"                   // 闪
bind "c" "slot8"                   // 烟
bind "6" "slot9"                   // 诱饵弹
bind "x" "slot10"                  // 火
// bind "q" "lastinv"                 // 切换到上一个武器
bind "y" "+spray_menu"             // 打开喷漆菜单
bind "i" "messagemode2"            // 打开团队聊天
bind "u" "messagemode"             // 打开全局聊天
bind "v" "+voicerecord"       // 语音
bind "mouse3" "player_ping"        // 玩家标记
bind "mwheeldown" "invnext"          // 鼠标滚轮切换装备
bind "mwheelup" "invprev"            // 鼠标滚轮切换装备
bind "`" "toggleconsole"                           // 打开/关闭控制台
bind "h" "switchhands"                             // 切换武器持握方式（左手/右手）
bind "t" "toggleradarscale"                        // 切换雷达缩放比例
bind "alt" "toggle cl_teamid_overhead_mode 1 3"    // 切换队友头顶标识模式
bind "ralt" "radio2;slot12"                        // 打开无线电菜单、X光显示、医疗针
bind "-" "toggle cl_draw_only_deathnotices 1 0"    // 切换是否仅显示死亡通知与准星
bind "=" "toggle cl_drawhud_force_radar 1 0"       // 切换是否强制显示雷达
bind F1 "vote 1"                                   // 投票选择同意
bind F2 "vote 2"                                   // 投票选择拒绝
bind "f5" "buy hegrenade"                          // 购买高爆手雷
bind "f6" "buy flashbang"                          // 购买闪光弹
bind "f7" "buy smokegrenade"                       // 购买烟雾弹
bind "f8" "buy molotov;buy incgrenade"             // 购买燃烧瓶/燃烧弹
bind "f9" "buy vest"                               // 购买防弹衣
bind "f10" "buy vesthelm"                          // 购买防弹衣+头盔
bind "f11" "buy defuser"                           // 购买拆弹器
bind "f4" "buy rifle1"                             // 购买主武器（步枪）
bind "f3" "buy secondary4"                         // 购买副武器（手枪）
bind "f12" "sellbackall"                           // 出售所有已购买物品
//cfg
exec zeus.cfg
bind "o" "exec crosshair_view;say_team crosshair_view!"
bind "\" "say_team keys_log!;echoln "CFG按键指示";echoln "- 自启动：zeus电击枪快速切换";echoln "- o：autoexec重启配置";echoln "- j：knife匕首模型轮换";echoln "- p：train跑图模式";echoln "- [：crosshair轮换准星设置";echoln "- ]：view轮换持枪视角";echoln "- /：lastinv弯刀检视优化";echoln "- k：一键发刀";echoln "- o：默认准星与视角""
bind "j" "exec knife.cfg;say_team knife_model!"
bind "p" "exec train.cfg;say_team train_model!"
bind "[" "exec crosshair_view;say_team crosshair_view!"
bind "]" "exec crosshair_view;say_team crosshair_view!"
bind "/" "exec lastinv.cfg;say_team lastinv!"
bind "k" "say_team !drop"
//准星
cl_crosshair_drawoutline "false"                     // 禁用准星轮廓绘制
cl_crosshair_dynamic_maxdist_splitratio "0.300000"   // 动态准星最大分离距离的比例
cl_crosshair_dynamic_splitalpha_innermod "1.000000"  // 动态准星内部分离部分的透明度
cl_crosshair_dynamic_splitalpha_outermod "0.500000"  // 动态准星外部分离部分的透明度
cl_crosshair_dynamic_splitdist "7"                   // 动态准星分离距离
cl_crosshair_outlinethickness "1.000000"             // 准星轮廓的厚度（如果启用轮廓）
cl_crosshair_recoil "false"                          // 禁用准星随武器后坐力动态变化
cl_crosshair_t "false"                               // 禁用T形准星
cl_crosshairalpha "255"                              // 准星的透明度（255为完全不透明）
cl_crosshaircolor "5"                                // 准星颜色（5为自定义颜色）
cl_crosshaircolor_b "255"                            // 准星颜色的蓝色分量（RGB）
cl_crosshaircolor_g "255"                            // 准星颜色的绿色分量（RGB）
cl_crosshaircolor_r "255"                            // 准星颜色的红色分量（RGB）
cl_crosshairdot "false"                              // 禁用准星中心点
cl_crosshairgap "-3.400000"                          // 准星间隙大小（负值表示准星向内收缩）
cl_crosshairgap_useweaponvalue "false"               // 禁用根据武器调整准星间隙
cl_crosshairsize "0.900000"                          // 准星大小
cl_crosshairstyle "4"                                // 准星样式（4为经典静态准星）
cl_crosshairthickness "0.800000"                     // 准星线条的厚度
cl_crosshairusealpha "true"                          // 启用准星透明度设置
cl_crosshair_sniper_width "2"						 // 狙击镜准星线粗细
//投掷物准星
cl_fixedcrosshaigap "3"                   // 设置固定准星的间隙大小
cl_grenadecrosshair_decoy 1               // 启用诱饵弹的投掷轨迹准星
cl_grenadecrosshair_explosive 1           // 启用爆炸物（如手雷）的投掷轨迹准星
cl_grenadecrosshair_fire 1                // 启用燃烧弹的投掷轨迹准星
cl_grenadecrosshair_flash 1               // 启用闪光弹的投掷轨迹准星
cl_grenadecrosshair_keepusercrosshair 1   // 投掷时保留玩家自定义准星
cl_grenadecrosshair_smoke 1               // 启用烟雾弹的投掷轨迹准星
cl_grenadecrosshairdelay_decoy "0.114345" // 设置诱饵弹投掷轨迹准星的延迟时间
cl_grenadecrosshairdelay_explosive "0.114345" // 设置爆炸物投掷轨迹准星的延迟时间
cl_grenadecrosshairdelay_fire "0.114345"  // 设置燃烧弹投掷轨迹准星的延迟时间
cl_grenadecrosshairdelay_flash "0.114345" // 设置闪光弹投掷轨迹准星的延迟时间
cl_grenadecrosshairdelay_smoke "0.114345" // 设置烟雾弹投掷轨迹准星的延迟时间
//其余准星设置
cl_observed_bot_crosshair 2               // 观察机器人时显示准星（2为始终显示）
cl_show_observer_crosshair 2              // 观察其他玩家时显示准星（2为始终显示）
cl_teamid_overhead_fade_near_crosshair "0.5" // 设置队友ID在准星附近时的淡出距离
//持枪视角
viewmodel_fov 68                  // 设置视角模型（武器）的视野范围
viewmodel_offset_x 2              // 调整视角模型在X轴上的偏移（左右位置）
viewmodel_offset_y 2              // 调整视角模型在Y轴上的偏移（前后位置）
viewmodel_offset_z -1             // 调整视角模型在Z轴上的偏移（上下位置）
viewmodel_presetpos 0             // 禁用预设的视角模型位置，允许自定义偏移
//雷达
cl_radar_always_centered "0"        // 雷达不居中，显示整个地图
cl_radar_scale "0.37"               // 设置雷达缩放比例为 0.37
cl_hud_radar_scale "1"              // 设置 HUD 雷达缩放比例为 1
cl_teammate_colors_show "2"         // 显示队友颜色为 2（默认颜色模式）
cl_radar_icon_scale_min "0.6"       // 设置雷达图标最小缩放比例为 0.6
cl_radar_rotate "1"                 // 雷达随玩家视角旋转
//网络
cl_hud_telemetry_frametime_show 2  // 显示帧生成时间及FPS
cl_hud_telemetry_ping_show 2       // 显示延迟
mm_dedicated_search_maxping "70"   // 设置匹配时允许的最大 ping 值
//功能
cl_prefer_lefthanded 0             // 右手持枪（默认）
cl_debounce_zoom 0                 // 按住开镜键持续切换
cl_silencer_mode 1                 // 开启卸下消音器
cl_use_opens_buy_menu "0"          // 关闭E键打开购买菜单
cl_dm_buyrandomweapons 0           // 关闭死斗随机买枪
cl_teamcounter_playercount_instead_of_avatars 1 // 显示对局存活数字
r_drawtracers_firstperson 1        // 显示曳光弹
r_fullscreen_gamma 2.6             // 设置亮度
cl_teamid_overhead_mode 3          // 隔墙显示队友位置
cl_teamid_overhead_colors_show 1   // 玩家ID上使用玩家颜色
//声音
volume 1                              // 主音量
snd_headphone_eq 0                    // 均衡器
snd_menumusic_volume 0.03             // 主菜单音乐音量
snd_roundstart_volume 0               // 回合开始音量
snd_roundend_volume 0.02              // 回合结束音量
snd_roundaction_volume 0              // 回合开始行动音量
snd_mvp_volume 0.12                   // MVP音量
snd_mapobjective_volume 0.12          // 炸弹/人质音量
snd_tensecondwarning_volume 0.08      // 十秒警告音量
snd_deathcamera_volume 0.08           // 死亡视角音量
snd_mute_mvp_music_live_players 1     // 当双方团队成员都存活时关闭 MVP 音乐
snd_mute_losefocus 0                  // 后台播放声音
voice_modenable 1                     // 启用语音
//HUD
hud_showtargetid "1"               // 显示队友/敌人的 ID
hud_scaling "0.85"                 // 设置 HUD 缩放比例
safezonex "0.88"                   // 设置 HUD 水平占比
safezoney "0.905"                  // 设置 HUD 竖直占比
cl_color "4"                       // 设置队伍中玩家颜色
cl_hud_color "11"                  // 设置 HUD 颜色
cl_showloadout "0"                 // 不总显示物品栏
//其他
con_enable "1"                     // 启用开发者控制台
fps_max 0                          // 帧率无上限
cl_join_advertise "2"              // 公开游戏会话
gameinstructor_enable "0"          // 禁用教学提示系统
cl_autohelp "false"                // 禁用自动帮助提示
func_break_max_pieces 0            // 可破坏物体破碎时最大碎片数
r_show_build_info 0                // 关闭版本信息
spec_replay_autostart 0            // 关闭被击杀回放
//Ending
echo AutoConfig Enabled!
```

## train.cfg
- 单人跑图
```ini
//Train
unbind F1
unbind F2
unbind F3
unbind F4
unbind F5
unbind F6
unbind F7
unbind F8
unbind MOUSE4
bind "k" "toggle cl_showpos 0 1"                   // 显示位置速度信息
bind "l" "sv_rethrow_last_grenade"重投上一个道具
bind "n" "noclip"
bind F4 bot_add  //按F4添加一个随机阵营的机器人，第一个一般是与你相对阵营的
bind F8 bot_kick  //按F8移除所有机器人
bind MOUSE4 bot_place  //按侧键在准心处放置一个机器人
bind F5 "toggle bot_crouch"  //按F5所有机器人站姿、蹲姿切换
bind F6 "toggle bot_mimic 0 -1   //机器人模仿动作
bind F7 "toggle fov_cs_debug 0 30"  //放大视野，投掷物找瞄点使用
bind , "ent_fire smokegrenade_projectile kill;ent_fire flashbang_projectile kill;ent_fire incgrenade_projectile kill;ent_fire molotov_projectile kill;ent_fire hegrenade_projectile kill;ent_fire decoy_projectile kill;stopsound"  //清除投掷物，燃烧弹、燃烧瓶碰地后无法清楚
bind F1 "give item_assaultsuit" //补甲
bind "F2" "toggle sv_regeneration_force_on 0 1"//切换自动回血
bind "F3" "toggle sv_falldamage_scale 0 1"//切换掉落伤害有无
alias "spawn" "exec spawn/spawn.cfg"//控制台输入spawn，启用spawn.cfg
say_team 正在加载跑图模式...
echoln "==========================================================="
echoln "                    跑图模式功能列表                    "
echoln "==========================================================="
echoln ""
echoln "【BOT相关命令】"
echoln "  > BOT "
echoln "    - F8：移除所有机器人"
echoln "    - F4：添加随机阵营机器人"
echoln "    - MOUSE4：在准心处放置机器人"
echoln "    - F5：切换机器人站姿/蹲姿"
echoln "    - F6：切换机器人动作模仿"
echoln ""
echoln "【道具相关命令】"
echoln "    - ,：清除所有投掷物"
echoln "    - l：重投上一个道具"
echoln ""
echoln "【实用功能命令】"
echoln "    - F3: 快速切换摔落伤害"
echoln "    - F7: 放大视野功能"
echoln "    - n: 穿墙功能"
echoln "    - F1: 补充护甲"
echoln "    - F2: 自动回血"
echoln "  > spawn - 启用出生点CFG"
echoln ""
echoln "加载完成，祝您发现更多新鲜道具和战术！"
ammo_grenade_limit_total 5 投掷物最大携带数量调整为5个
bot_kick  //移除机器人
bot_stop 1  //机器人静止
bot_join_after_player 1      //BOT在玩家后加入
bot_chatter 0      //关闭BOT语音
cl_versus_intro 0 //移除开场动画
mp_autokick 0  //禁用自动踢出
sv_maxplayers 32  //最大玩家数量调整为32
mp_autoteambalance 0  //禁用队伍不平衡
mp_buy_anywhere 1  //随处可以购买
mp_buytime 9999999  //购买时间无限
mp_ct_default_grenades "weapon_flashbang weapon_hegrenade weapon_smokegrenade weapon_incgrenade weapon_decoy"  //CT方自带道具
mp_death_drop_grenade 0  //死亡后不掉落投掷物
mp_death_drop_gun 1  //死亡掉枪
mp_death_drop_defuser 0  //死亡不掉钳子
mp_drop_knife_enable 1  //允许丢弃刀
mp_free_armor 0  //出生不带甲
mp_freezetime 0  //开局冻结时间为0
mp_friendlyfire 0  //禁用友伤
mp_ignore_round_win_conditions 1  //禁用胜利条件，不会结束游戏
mp_limitteams 10  //队伍最大人数差为10
mp_maxmoney 99999  //最大金钱数99999
mp_maxrounds 999999 //最大回合数999999
mp_respawn_on_death_ct 1  //CT死后允许复活
mp_respawn_on_death_t 1  //T死后允许复活
mp_respawnwavetime_ct 1  //CT复活时间为1秒
mp_respawnwavetime_t 1  //T复活时间为1秒
mp_roundtime 60  //回合时间60min
mp_roundtime_defuse 60  //竞技模式回合时间60min
mp_roundtime_hostage 60  //人质模式回合时间60min
mp_solid_teammates 1  //不允许穿过队友身体
mp_spectators_max 9  //最大观察者9个
mp_startmoney 99999  //初始金钱99999
mp_t_default_grenades "weapon_flashbang weapon_hegrenade weapon_smokegrenade weapon_molotov weapon_decoy"  //T方自带道具
mp_t_default_primary weapon_ak47
mp_t_default_secondary weapon_deagle
mp_ct_default_primary weapon_m4a4
mp_ct_default_secondary weapon_deagle
mp_team_intro_time 0  //跳过开局队伍动画
mp_weapons_allow_typecount -1 //无限购买武器
mp_warmup_end  //结束热身
sv_alltalk 1  //双方语言互通
sv_cheats 1  //开启作弊
sv_grenade_trajectory_prac_pipreview 1  //预览投掷物窗口
sv_grenade_trajectory_prac_trailtime 8  //投掷物轨迹持续8秒
sv_grenade_trajectory_time_spectator 4  //弹痕显示时长为4秒
sv_infinite_ammo 2  //无限备弹
sv_showimpacts 1  //显示服务器子弹碰撞判定箱
sv_showimpacts_time 5  //显示服务器子弹碰撞判定箱时间为5秒
mp_restartgame 1  //重启房间
say_team Practice Enabled
```

- “p”键启用，参考于 **Bad0RANG3** ，项目地址：https://github.com/Bad0RANG3/CS2PraticeCFG ，个人空间：https://space.bilibili.com/482966540

---

> 注意以下 cfg 都需要存放在游戏全局 cfg 文件夹下的 spawn 文件夹内，比如 **...\SteamLibrary\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\spawn** 或 **...\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\spawn** 下。

### spawn.cfg
- 重生点预设置
```ini
// CS2 Spawn Positions Config
// 初始化变量
exec spawn/init_spawns.cfg
// 地图配置文件
alias "dust2" "exec spawn/dust2.cfg"
alias "inferno" "exec spawn/inferno.cfg"
alias "mirage" "exec spawn/mirage.cfg"
alias "ancient" "exec spawn/ancient.cfg"
alias "nuke" "exec spawn/nuke.cfg"
alias "vertigo" "exec spawn/vertigo.cfg"
alias "anubis" "exec spawn/anubis.cfg"
alias "office" "exec spawn/office.cfg"
alias "italy" "exec spawn/italy.cfg"
alias "pool_day" "exec spawn/pool_day.cfg"
alias "shoots" "exec spawn/shoots.cfg"
alias "baggage" "exec spawn/baggage.cfg"
// 使用说明
echo "=== CS2 出生点配置使用说明 ==="
echo "1. 输入地图名称(如: dust2)来加载对应地图的出生点"
echo "2. 加载后使用CT1-CT20或T1-T20来传送到对应出生点"
echo "==========================="
// 地图中英文对照说明
echo "=== 地图中英文对照说明 ==="
echo "+----------+------------+"
echo "| 英文名称 | 中文名称   |"
echo "+----------+------------+"
echo "| dust2    | 沙漠2     |"
echo "| inferno  | 炼狱小镇   |"
echo "| mirage   | 荒漠迷城   |"
echo "| ancient  | 远古遗迹   |"
echo "| nuke     | 核子危机   |"
echo "| vertigo  | 殒命大厦   |"
echo "| anubis   | 阿努比斯   |"
echo "| office   | 办公室     |"
echo "| italy    | 意大利     |"
echo "| pool_day | 泳池日     |"
echo "| shoots   | 射击训练   |"
echo "| baggage  | 行李仓库   |"
echo "+----------+------------+"
```

### vertigo.cfg
- 殒命大厦重生点
```ini
// Vertigo出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact -860.1436 940.28204 11789;setang 0 301.00003 0;say \"已传送至: Vertigo - CT点 1号位置\""
alias "CT2" "setpos_exact -929.6314 918.6384 11789;setang 0 329.00003 0;say \"已传送至: Vertigo - CT点 2号位置\""
alias "CT3" "setpos_exact -1189.3397 862.16864 11789;setang 0 9.499999 0;say \"已传送至: Vertigo - CT点 3号位置\""
alias "CT4" "setpos_exact -1126.5762 925.89246 11789;setang 0 307.00006 0;say \"已传送至: Vertigo - CT点 4号位置\""
alias "CT5" "setpos_exact -1044.0262 924.3055 11789;setang 0 279.5 0;say \"已传送至: Vertigo - CT点 5号位置\""
alias "T1" "setpos_exact -1411.3145 -1130.3131 11505;setang 0 317.5 0;say \"已传送至: Vertigo - T点 1号位置\""
alias "T2" "setpos_exact -1502.5718 -1360.8275 11505;setang 0 171.99994 0;say \"已传送至: Vertigo - T点 2号位置\""
alias "T3" "setpos_exact -1439.7609 -1322.0359 11505;setang 0 193.50003 0;say \"已传送至: Vertigo - T点 3号位置\""
alias "T4" "setpos_exact -1439.5718 -1251.7084 11505;setang 0 243.00003 0;say \"已传送至: Vertigo - T点 4号位置\""
alias "T5" "setpos_exact -1468.8372 -1194.3975 11505;setang 0 272.5 0;say \"已传送至: Vertigo - T点 5号位置\""
say "地图: Vertigo | CT: 5个出生点 | T: 5个出生点"
```

### office.cfg
- 办公室重生点
```ini
// Office出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact 1800 2100 -100;setang 0 270 0;say \"已传送至: Office - CT点 1号位置\""
alias "CT2" "setpos_exact 1800 2000 -100;setang 0 270 0;say \"已传送至: Office - CT点 2号位置\""
alias "CT3" "setpos_exact 1800 1900 -100;setang 0 270 0;say \"已传送至: Office - CT点 3号位置\""
alias "CT4" "setpos_exact 1700 2050 -100;setang 0 270 0;say \"已传送至: Office - CT点 4号位置\""
alias "CT5" "setpos_exact 1700 1950 -100;setang 0 270 0;say \"已传送至: Office - CT点 5号位置\""
alias "T1" "setpos_exact -1800 1000 -100;setang 0 90 0;say \"已传送至: Office - T点 1号位置\""
alias "T2" "setpos_exact -1800 900 -100;setang 0 90 0;say \"已传送至: Office - T点 2号位置\""
alias "T3" "setpos_exact -1800 800 -100;setang 0 90 0;say \"已传送至: Office - T点 3号位置\""
alias "T4" "setpos_exact -1700 950 -100;setang 0 90 0;say \"已传送至: Office - T点 4号位置\""
alias "T5" "setpos_exact -1700 850 -100;setang 0 90 0;say \"已传送至: Office - T点 5号位置\""
say "地图: Office | CT: 5个出生点 | T: 5个出生点"
```

### nuke.cfg
- 核子危机重生点
```ini
// Nuke出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact 2504 -344 -335;setang 0 271 0;say \"已传送至: Nuke - CT点 1号位置\""
alias "CT2" "setpos_exact 2552 -424 -335;setang 0 207.5 0;say \"已传送至: Nuke - CT点 2号位置\""
alias "CT3" "setpos_exact 2512 -504 -335;setang 0 145 0;say \"已传送至: Nuke - CT点 3号位置\""
alias "CT4" "setpos_exact 2585 -344 -335;setang 0 200.5 0;say \"已传送至: Nuke - CT点 4号位置\""
alias "CT5" "setpos_exact 2584 -504 -335;setang 0 161 0;say \"已传送至: Nuke - CT点 5号位置\""
alias "T1" "setpos_exact -1808 -1025 -400.634;setang 0 329 0;say \"已传送至: Nuke - T点 1号位置\""
alias "T2" "setpos_exact -1947.01 -965.11 -400.634;setang 0 312 0;say \"已传送至: Nuke - T点 2号位置\""
alias "T3" "setpos_exact -1947.01 -1102.11 -400.634;setang 0 74.5 0;say \"已传送至: Nuke - T点 3号位置\""
alias "T4" "setpos_exact -1878 -980 -400.634;setang 0 294 0;say \"已传送至: Nuke - T点 4号位置\""
alias "T5" "setpos_exact -1832 -1160 -400.634;setang 0 40 0;say \"已传送至: Nuke - T点 5号位置\""
alias "T6" "setpos_exact -1929 -1025 -400.634;setang 0 3 0;say \"已传送至: Nuke - T点 6号位置\""
alias "T7" "setpos_exact -1874 -1076 -400.634;setang 0 336 0;say \"已传送至: Nuke - T点 7号位置\""
alias "T8" "setpos_exact -1808 -1089 -400.634;setang 0 340 0;say \"已传送至: Nuke - T点 8号位置\""
say "地图: Nuke | CT: 5个出生点 | T: 8个出生点"
```

### mirage.cfg
- 荒漠迷城重生点
```ini
// Mirage出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact -1776 -1976 -240;setang 0 331 0;say \"已传送至: Mirage - CT点 1号位置\""
alias "CT2" "setpos_exact -1776 -1800 -240;setang 0 36 0;say \"已传送至: Mirage - CT点 2号位置\""
alias "CT3" "setpos_exact -1720 -1896 -240;setang 0 50 0;say \"已传送至: Mirage - CT点 3号位置\""
alias "CT4" "setpos_exact -1656 -1800 -240;setang 0 94 0;say \"已传送至: Mirage - CT点 4号位置\""
alias "CT5" "setpos_exact -1656 -1976 -240;setang 0 299 0;say \"已传送至: Mirage - CT点 5号位置\""
alias "T1" "setpos_exact 1296 -352 -144;setang 0 227 0;say \"已传送至: Mirage - T点 1号位置\""
alias "T2" "setpos_exact 1296 32 -144;setang 0 141 0;say \"已传送至: Mirage - T点 2号位置\""
alias "T3" "setpos_exact 1216 -16 -144;setang 0 90 0;say \"已传送至: Mirage - T点 3号位置\""
alias "T4" "setpos_exact 1216 -115 -144;setang 0 90 0;say \"已传送至: Mirage - T点 4号位置\""
alias "T5" "setpos_exact 1216 -211 -144;setang 0 270 0;say \"已传送至: Mirage - T点 5号位置\""
alias "T6" "setpos_exact 1216 -307 -144;setang 0 270 0;say \"已传送至: Mirage - T点 6号位置\""
alias "T7" "setpos_exact 1136 -256 -144;setang 0 270 0;say \"已传送至: Mirage - T点 7号位置\""
alias "T8" "setpos_exact 1136 -160 -144;setang 0 270 0;say \"已传送至: Mirage - T点 8号位置\""
alias "T9" "setpos_exact 1136 -64 -144;setang 0 90 0;say \"已传送至: Mirage - T点 9号位置\""
alias "T10" "setpos_exact 1136 32 -144;setang 0 90 0;say \"已传送至: Mirage - T点 10号位置\""
say "地图: Mirage | CT: 5个出生点 | T: 10个出生点"
```

### italy.cfg
- 意大利重生点
```ini
// Italy出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact 1200 2300 100;setang 0 270 0;say \"已传送至: Italy - CT点 1号位置\""
alias "CT2" "setpos_exact 1200 2200 100;setang 0 270 0;say \"已传送至: Italy - CT点 2号位置\""
alias "CT3" "setpos_exact 1200 2100 100;setang 0 270 0;say \"已传送至: Italy - CT点 3号位置\""
alias "CT4" "setpos_exact 1100 2250 100;setang 0 270 0;say \"已传送至: Italy - CT点 4号位置\""
alias "CT5" "setpos_exact 1100 2150 100;setang 0 270 0;say \"已传送至: Italy - CT点 5号位置\""
alias "T1" "setpos_exact -1200 800 100;setang 0 90 0;say \"已传送至: Italy - T点 1号位置\""
alias "T2" "setpos_exact -1200 700 100;setang 0 90 0;say \"已传送至: Italy - T点 2号位置\""
alias "T3" "setpos_exact -1200 600 100;setang 0 90 0;say \"已传送至: Italy - T点 3号位置\""
alias "T4" "setpos_exact -1100 750 100;setang 0 90 0;say \"已传送至: Italy - T点 4号位置\""
alias "T5" "setpos_exact -1100 650 100;setang 0 90 0;say \"已传送至: Italy - T点 5号位置\""
say "地图: Italy | CT: 5个出生点 | T: 5个出生点"
```

### inferno.cfg
- 炼狱小镇重生点
```ini
// Inferno出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact 2292.06 2027.69 140.843;setang 0 70 0;say \"已传送至: Inferno - CT点 1号位置\""
alias "CT2" "setpos_exact 2353 1977 140.843;setang 0 97.5 0;say \"已传送至: Inferno - CT点 2号位置\""
alias "CT3" "setpos_exact 2397 2079 155;setang 0 135 0;say \"已传送至: Inferno - CT点 3号位置\""
alias "CT4" "setpos_exact 2472.3499 2005.97 140.843;setang 0 160 0;say \"已传送至: Inferno - CT点 4号位置\""
alias "CT5" "setpos_exact 2493 2090 140.843;setang 0 223.5 0;say \"已传送至: Inferno - CT点 5号位置\""
alias "CT6" "setpos_exact 2456.83 2153.16 140.843;setang 0 251.5 0;say \"已传送至: Inferno - CT点 6号位置\""
alias "T1" "setpos_exact -1586.52 440.79 -46;setang 0 337 0;say \"已传送至: Inferno - T点 1号位置\""
alias "T2" "setpos_exact -1520.06 430.891 -46;setang 0 267 0;say \"已传送至: Inferno - T点 2号位置\""
alias "T3" "setpos_exact -1657.23 419.577 -46;setang 0 358.5 0;say \"已传送至: Inferno - T点 3号位置\""
alias "T4" "setpos_exact -1675.62 351.695 -46;setang 0 48 0;say \"已传送至: Inferno - T点 4号位置\""
alias "T5" "setpos_exact -1662.18 288.762 -46;setang 0 77.5 0;say \"已传送至: Inferno - T点 5号位置\""
say "地图: Inferno | CT: 6个出生点 | T: 5个出生点"
```

### dust2.cfg
- 沙漠2重生点
```ini
// Dust2出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置出生点数量
alias "max_ct_spawns" "5"
alias "max_t_spawns" "15"
// 初始化变量
exec spawn/init_spawn_vars.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact 182.24991 2439.0117 -110;setang 0 356 0;say \"已传送至: Dust2 - CT点 1号位置\""
alias "CT2" "setpos_exact 160.12274 2369.6763 -110;setang 0 23.999994 0;say \"已传送至: Dust2 - CT点 2号位置\""
alias "CT3" "setpos_exact 258.1594 2480.5537 -110;setang 0 292.5 0;say \"已传送至: Dust2 - CT点 3号位置\""
alias "CT4" "setpos_exact 334.36874 2433.7336 -110;setang 0 229.99998 0;say \"已传送至: Dust2 - CT点 4号位置\""
alias "CT5" "setpos_exact 351.39212 2352.9424 -110;setang 0 202.5 0;say \"已传送至: Dust2 - CT点 5号位置\""
alias "T1" "setpos_exact -822.3652 -795.6421 150.709;setang 0 106.99999 0;say \"已传送至: Dust2 - T点 1号位置\""
alias "T2" "setpos_exact -857.50653 -738.3613 150.709;setang 0 37 0;say \"已传送至: Dust2 - T点 2号位置\""
alias "T3" "setpos_exact -760.66296 -836.174 150.709;setang 0 128.49997 0;say \"已传送至: Dust2 - T点 3号位置\""
alias "T4" "setpos_exact -696.8446 -806.6237 150.709;setang 0 178 0;say \"已传送至: Dust2 - T点 4号位置\""
alias "T5" "setpos_exact -657.27136 -755.87964 150.709;setang 0 207.50002 0;say \"已传送至: Dust2 - T点 5号位置\""
alias "T6" "setpos_exact -1141 -808 150.709;setang 0 111.99999 0;say \"已传送至: Dust2 - T点 6号位置\""
alias "T7" "setpos_exact -1181 -754 150.709;setang 0 42 0;say \"已传送至: Dust2 - T点 7号位置\""
alias "T8" "setpos_exact -1076 -843 150.709;setang 0 133.49998 0;say \"已传送至: Dust2 - T点 8号位置\""
alias "T9" "setpos_exact -1015 -808 150.709;setang 0 183.00002 0;say \"已传送至: Dust2 - T点 9号位置\""
alias "T10" "setpos_exact -657.271362 -755.879639 119.884018;setang_exact 0.000000 -152.499847 0.000000;say \"已传送至: Dust2 - T点 10号位置\""
alias "T11" "setpos_exact -533.000000 -754.000000 113.848984;setang_exact 0.000000 42.000046 0.000000;say \"已传送至: Dust2 - T点 11号位置\""
alias "T12" "setpos_exact -493.000000 -808.000000 108.563377;setang_exact 0.000000 112.000122 0.000000;say \"已传送至: Dust2 - T点 12号位置\""
alias "T13" "setpos_exact -428.000000 -843.000000 95.296295;setang_exact 0.000000 133.500031 0.000000;say \"已传送至: Dust2 - T点 13号位置\""
alias "T14" "setpos_exact -367.000000 -808.000000 83.744965;setang_exact 0.000000 -177.000046 0.000000;say \"已传送至: Dust2 - T点 14号位置\""
alias "T15" "setpos_exact -332.000000 -754.000000 78.877106;setang_exact 0.000000 -147.500031 0.000000;say \"已传送至: Dust2 - T点 15号位置\""
say "地图: Dust2 | CT: 5个出生点 | T: 15个出生点"
```

### anubis.cfg
- 阿努比斯重生点
```ini
// Anubis出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact -400 2192 32.0001;setang 0 240 0;say \"已传送至: Anubis - CT点 1号位置\""
alias "CT2" "setpos_exact -560 2192 32;setang 0 285 0;say \"已传送至: Anubis - CT点 2号位置\""
alias "CT3" "setpos_exact -476 2216 32;setang 0 270 0;say \"已传送至: Anubis - CT点 3号位置\""
alias "CT4" "setpos_exact -608 2120 32;setang 0 315 0;say \"已传送至: Anubis - CT点 4号位置\""
alias "CT5" "setpos_exact -360 2120 32.0001;setang 0 225 0;say \"已传送至: Anubis - CT点 5号位置\""
alias "T1" "setpos_exact -416 -1696 16;setang 0 135 0;say \"已传送至: Anubis - T点 1号位置\""
alias "T2" "setpos_exact -234 -1503.08 16;setang 0 45 0;say \"已传送至: Anubis - T点 2号位置\""
alias "T3" "setpos_exact -154 -1503.08 16;setang 0 30 0;say \"已传送至: Anubis - T点 3号位置\""
alias "T4" "setpos_exact -384 -1552 16;setang 0 165 0;say \"已传送至: Anubis - T点 4号位置\""
alias "T5" "setpos_exact -328 -1528 16;setang 0 150 0;say \"已传送至: Anubis - T点 5号位置\""
alias "T6" "setpos_exact -264 -1560 16;setang 0 90 0;say \"已传送至: Anubis - T点 6号位置\""
alias "T7" "setpos_exact -144 -1568 16;setang 0 60 0;say \"已传送至: Anubis - T点 7号位置\""
alias "T8" "setpos_exact -128.004 -1632 16;setang 0 45 0;say \"已传送至: Anubis - T点 8号位置\""
alias "T9" "setpos_exact -416 -1608 16;setang 0 150 0;say \"已传送至: Anubis - T点 9号位置\""
alias "T10" "setpos_exact -304 -1608 16;setang 0 135 0;say \"已传送至: Anubis - T点 10号位置\""
alias "T11" "setpos_exact -192 -1608 16;setang 0 90 0;say \"已传送至: Anubis - T点 11号位置\""
say "地图: Anubis | CT: 5个出生点 | T: 11个出生点"
```

### ancient.cfg
- 远古遗迹重生点
```ini
// Ancient出生点配置
// 初始化所有出生点
exec spawn/init_spawns.cfg
// 设置可用的出生点
alias "CT1" "setpos_exact -192 1696 32;setang 0 270 0;say \"已传送至: Ancient - CT点 1号位置\""
alias "CT2" "setpos_exact -256 1728 32;setang 0 270 0;say \"已传送至: Ancient - CT点 2号位置\""
alias "CT3" "setpos_exact -352 1728 32;setang 0 270 0;say \"已传送至: Ancient - CT点 3号位置\""
alias "CT4" "setpos_exact -448 1728 32;setang 0 270 0;say \"已传送至: Ancient - CT点 4号位置\""
alias "CT5" "setpos_exact -512 1696 32;setang 0 270 0;say \"已传送至: Ancient - CT点 5号位置\""
alias "T1" "setpos_exact -328 -2288 -156;setang 0 90 0;say \"已传送至: Ancient - T点 1号位置\""
alias "T2" "setpos_exact -456 -2288 -156;setang 0 90 0;say \"已传送至: Ancient - T点 2号位置\""
alias "T3" "setpos_exact -584 -2288 -156;setang 0 90 0;say \"已传送至: Ancient - T点 3号位置\""
alias "T4" "setpos_exact -392 -2224 -156;setang 0 90 0;say \"已传送至: Ancient - T点 4号位置\""
alias "T5" "setpos_exact -520 -2224 -156;setang 0 90 0;say \"已传送至: Ancient - T点 5号位置\""
say "地图: Ancient | CT: 5个出生点 | T: 5个出生点"
```

### init_spawns.cfg
- 重生点初始化
```ini
// 初始化CT出生点
alias "CT1" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT2" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT3" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT4" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT5" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT6" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT7" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT8" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT9" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT10" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT11" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT12" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT13" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT14" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "CT15" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
// 初始化T出生点
alias "T1" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T2" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T3" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T4" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T5" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T6" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T7" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T8" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T9" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T10" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T11" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T12" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T13" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T14" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
alias "T15" "echo \"没有这个出生点，请检查该地图的出生点个数以选择\""
```

---

## demo.cfg
- 看demo专用，集成了一些实用指令的快捷键
- 取自 Purp1e 老师：https://space.bilibili.com/73115492

```ini
// ═══════════════════════════════════════════
//        Config Preset v2.6b by Purp1e
//            CFG预设（Purp1e制作）
//                #2024/11/10#
//     https://space.bilibili.com/73115492
// ═══════════════════════════════════════════
// ─────────────────────────  绑定键位  ──────────────────────────────────
binddefaults;                                                // 重置所有按键，以防键位冲突，bind指令必须放在之后↓
bind q      "demoui"                                         // q 打开/关闭 demoui
bind h      "toggle cl_draw_only_deathnotices";              // h 只保留准星击杀
bind k      "toggle voice_modenable";                        // k 开关语音 解说语言要手动从Tab里开启
bind p      "demo_togglepause";                              // p 切换demo暂停/继续
bind mouse3 "demo_togglepause";                              // 鼠标中键 切换demo暂停/继续
bind mouse5 "gear_up";                                       // 前侧键 +播放速度
bind mouse4 "gear_down";                                     // 后侧键 -播放速度
bind v      "toggle crosshair 0 1";                          // v 隐藏准心
bind b      "toggle cl_drawhud";                             // b 隐藏所有hud包括击杀
bind n      "toggle cl_drawhud_force_radar 1 -1";            // n 开关雷达
bind m      "toggle host_timescale";                         // m 开关声音
bind pgup   "ScreenRecord;demo_resume; echo >>> 录屏开始"     // PageUp   (OBS..)录屏开始 需要录屏软件设置同样快捷键
bind pgdn   "fps_max 200;demo_timescale 1;demo_pause;echo >>> 录屏结束" // PageDown (OBS..)录屏结束
// ──────────────────────────  一次性命令  ──────────────────────────────
sv_cheats                  1      // 开启作弊
r_show_build_info          0      // 关闭版本信息
mp_display_kill_assists    1      // 显示助攻（0关闭）
engine_no_focus_sleep      0      // 窗口失焦/在后台时不掉帧
cl_show_observer_crosshair 0      // [观察时]显示玩家所用准星<0.否 1.好友及队友 2.所有人>
cl_showpos                 0      // 关闭位置信息
tv_listen_voice_indices   -1      // 开启玩家语音
demo_pause                        // 暂停demo
cl_hud_telemetry_frametime_show       0  // 显示帧生成时间及FPS <0.从不 1. 如果条件恶劣 2.总是>
cl_hud_telemetry_net_misdelivery_show 0  // 显示丢包/发送错误率LOSS <0.从不 1. 如果条件恶劣 2.总是>
cl_hud_telemetry_ping_show            0  // 显示延迟 <0.从不 1. 如果条件恶劣 2.总是>
cl_grenadecrosshair_decoy          0     // 是否显示诱饵弹准星，默认关闭
cl_grenadecrosshair_explosive      0     // 是否显示雷准星，默认关闭
cl_grenadecrosshair_fire           0     // 是否显示燃烧弹准星，默认关闭
cl_grenadecrosshair_flash          0     // 是否显示闪光弹准星，默认关闭
cl_grenadecrosshair_smoke          0     // 是否显示烟雾弹准星，默认关闭
// ─────────────────────────  HUD 准星 持枪  ─────────────────────────────
// 界面(HUD)设置 <0.默认 1.白色 2.淡蓝色 3.蓝色 4.紫色 5.红色 6.橙色 7.黄色 8.绿色 9.淡绿色 10.粉红色>
cl_hud_color              0       // 颜色
cl_radar_always_centered  1       // 雷达以玩家为中心
cl_radar_scale            0.45    // 雷达缩放
cl_hud_radar_scale        1       // 雷达大小（0.8-1.3）
cl_radar_icon_scale_min   0.6     // 雷达人物标点大小
cl_radar_rotate           1       // 雷达旋转
hud_showtargetid          0       // 隐藏目标id
// demo专用准星 [修改]
cl_crosshair_drawoutline "0"
cl_crosshair_dynamic_maxdist_splitratio "0.300000"
cl_crosshair_dynamic_splitalpha_innermod "1"
cl_crosshair_dynamic_splitalpha_outermod "0.5"
cl_crosshair_dynamic_splitdist "7"
cl_crosshair_friendly_warning "1"
cl_crosshair_outlinethickness "0.5"
cl_crosshair_sniper_width "1"
cl_crosshair_t "0"
cl_crosshairalpha "255"
cl_crosshaircolor "1"
cl_crosshaircolor_b "50"
cl_crosshaircolor_g "250"
cl_crosshaircolor_r "50"
cl_crosshairdot "0"
cl_crosshairgap "-0.500000"
cl_crosshairgap_useweaponvalue "0"
cl_crosshairsize "3.500000"
cl_crosshairstyle "4"
cl_crosshairthickness "1.000000"
cl_crosshairusealpha "1"
cl_fixedcrosshairgap "3"
// demo专用持枪视角参数
viewmodel_fov            "62"
viewmodel_offset_x       "2.5"
viewmodel_offset_y       "2"
viewmodel_offset_z       "-2"
viewmodel_presetpos      "0"
// ─────────────────────────  功能实现 ──────────────────────────────────
// 实现 修改 MVP、BGM等声音 静音的指令
alias mute "snd_menumusic_volume 0; snd_roundstart_volume 0;snd_roundend_volume 0;snd_roundaction_volume 0;snd_mapobjective_volume 0;snd_tensecondwarning_volume 0;snd_deathcamera_volume 0;snd_mvp_volume 0;snd_mute_mvp_music_live_players 1;snd_mute_losefocus 0";
// 实现 切换助攻显示
alias ass   "toggle mp_display_kill_assists; echo [切换助攻显示]"
// 实现 限制FPS
alias 60  "fps_max 60";
alias 90  "fps_max 90";
alias 120 "fps_max 120";
alias 200 "fps_max 200";
// 实现 前后侧键 +-播放速度 10% 20% 25% 100% 400% 800% 1600%
alias gear_up 	"gear4"
alias gear_down "gear14"
alias gear110   "demo_timescale 0.1; alias gear_up gear15;alias gear_down gear110;echo [Demo播放速度];echo X0.1"
alias gear15 	  "demo_timescale 0.2; alias gear_up gear14;alias gear_down gear110;echo [Demo播放速度];echo X0.2"
alias gear14	  "demo_timescale 0.25;alias gear_up gear1; alias gear_down gear15 ;echo [Demo播放速度];echo X0.25"
alias gear1     "demo_timescale 1;   alias gear_up gear4; alias gear_down gear14 ;echo [Demo播放速度];echo X1"
alias gear4     "demo_timescale 4;   alias gear_up gear8; alias gear_down gear1  ;echo [Demo播放速度];echo X4"
alias gear8     "demo_timescale 8;   alias gear_up gear8; alias gear_down gear4  ;echo [Demo播放速度];echo X8"
alias gear16    "demo_timescale 16;  alias gear_up gear16; alias gear_down gear8 ;echo [Demo播放速度];echo X16"
// 实现 录屏设置切换的快捷指令
alias 60to240     "alias ScreenRecord fps_max 60 ;demo_timescale 0.25 ;echo [当前录屏设置];echo 录制帧率=60 ;echo 播放速度=25%  ;echo 等效帧率=240"
alias 60to300     "alias ScreenRecord fps_max 60 ;demo_timescale 0.2  ;echo [当前录屏设置];echo 录制帧率=60 ;echo 播放速度=20%  ;echo 等效帧率=300"
alias 60to600     "alias ScreenRecord fps_max 60 ;demo_timescale 0.1  ;echo [当前录屏设置];echo 录制帧率=60 ;echo 播放速度=10%  ;echo 等效帧率=600"
alias 90to180     "alias ScreenRecord fps_max 90 ;demo_timescale 0.5  ;echo [当前录屏设置];echo 录制帧率=90 ;echo 播放速度=50%  ;echo 等效帧率=180"
alias 90to360     "alias ScreenRecord fps_max 90 ;demo_timescale 0.25 ;echo [当前录屏设置];echo 录制帧率=90 ;echo 播放速度=25%  ;echo 等效帧率=360"
alias 90to720     "alias ScreenRecord fps_max 90 ;demo_timescale 0.125;echo [当前录屏设置];echo 录制帧率=90 ;echo 播放速度=12.5%;echo 等效帧率=720"
alias 100to200    "alias ScreenRecord fps_max 100;demo_timescale 0.5  ;echo [当前录屏设置];echo 录制帧率=100;echo 播放速度=50%  ;echo 等效帧率=200"
alias 100to400    "alias ScreenRecord fps_max 100;demo_timescale 0.25 ;echo [当前录屏设置];echo 录制帧率=100;echo 播放速度=25%  ;echo 等效帧率=400"
alias 100to500    "alias ScreenRecord fps_max 100;demo_timescale 0.2  ;echo [当前录屏设置];echo 录制帧率=100;echo 播放速度=20%  ;echo 等效帧率=500"
alias 100to1000   "alias ScreenRecord fps_max 100;demo_timescale 0.1  ;echo [当前录屏设置];echo 录制帧率=100;echo 播放速度=10%  ;echo 等效帧率=1000"
alias 120to240    "alias ScreenRecord fps_max 120;demo_timescale 0.5  ;echo [当前录屏设置];echo 录制帧率=120;echo 播放速度=50%  ;echo 等效帧率=240"
alias 120to480    "alias ScreenRecord fps_max 120;demo_timescale 0.25 ;echo [当前录屏设置];echo 录制帧率=120;echo 播放速度=25%  ;echo 等效帧率=480"
alias 120to600    "alias ScreenRecord fps_max 120;demo_timescale 0.2  ;echo [当前录屏设置];echo 录制帧率=120;echo 播放速度=20%  ;echo 等效帧率=600"
alias 150to300    "alias ScreenRecord fps_max 150;demo_timescale 0.5  ;echo [当前录屏设置];echo 录制帧率=150;echo 播放速度=50%  ;echo 等效帧率=300"
alias 150to600    "alias ScreenRecord fps_max 600;demo_timescale 0.25 ;echo [当前录屏设置];echo 录制帧率=150;echo 播放速度=25%  ;echo 等效帧率=600"
alias 150         "alias ScreenRecord fps_max 150;demo_timescale 1    ;echo [当前录屏设置];echo 录制帧率=150;echo 播放速度=100% ;echo 等效帧率=150"
alias 300         "alias ScreenRecord fps_max 300;demo_timescale 1    ;echo [当前录屏设置];echo 录制帧率=300;echo 播放速度=100% ;echo 等效帧率=300"
//输出控制台提示
echo;
echo █▀▀█  █     █   █▀▀█  █▀▀█ ▄█   █▀▀▀    	█▀▀  █▀▀  █▀▀▀
echo █▄▄█  █     █   █▄▄▀  █▄▄█   █   █▀▀▀    	█       █▀▀  █  ▀█
echo █         ▀▄▄▀    █    █   █        ▄█▄ █▄▄▄   	▀▀▀  ▀       ▀▀▀▀	 v2.6b For CS2
echo ═════════════════════════════════════════════════════════════
echo ──── 加载设置[auto.cfg]	:  exec auto 或 auto
echo ──── 跑图,练习道具  		:  exec practice 或 pt
echo ──── 对枪,SOLO   		:  exec solo 或 solo
echo ──── 观战,观看DEMO,GOTV    	:  exec demo 或 demo
echo ──── 显示玩家所用准星   	:  cl_show_observer_crosshair 0  <0.否 1.好友及队友 2.所有人>
echo ──────────────────────  快捷键<开关式>  ────────────────────────
echo ──── 打开/关闭demoui        	:  q
echo ──── 侧边状态栏(血条、KDA)   	:  g
echo ──── HUD只保留准星和击杀    	:  h
echo ──── 开关语音      		:  k
echo ──── x光       	   	:  x
echo ──── 准心透明度      		:  v
echo ──── 开关HUD      		:  b
echo ──── 开关雷达      		:  n
echo ──── 静音           	 	:  m
echo ──── 快退5s      		:  ,
echo ──── 快进5s       		:  .
echo ──── demo暂停/继续           	:  p/鼠标中键（mouse3）
echo ─────────────────────  快捷键和指令  ───────────────────────────
echo ──── +播放速度      		:  前侧键（mouse5）
echo ──── - 播放速度      		:  后侧键（mouse4）
echo ──── 打开demoui      		:  shift+F2
echo ────────────────────────  指令  ──────────────────────────────
echo ──── 关闭BGM/MVP/无线电声音 	:  mute
echo ──── 切换助攻显示		:  ass
echo ──── 录屏慢放快捷指令		:  60to240 90to360 120to240等
echo ──── 限制FPS	           	:  60 → 限制 60FPS | 90 | 120 | 200
echo ═════════════════════════════════════════════════════════════
```

## knife.cfg
- 匕首模型更换
```ini
//knife_change
bind "j" "mp_drop_knife_enable 1;knife"
alias "knife" "knife1"
alias "knife1" "ent_fire weapon_knife changesubclass 500; alias knife knife2;say_team 已切换：刺刀"
alias "knife2" "ent_fire weapon_knife changesubclass 503; alias knife knife3;say_team 已切换：海豹短刀"
alias "knife3" "ent_fire weapon_knife changesubclass 505; alias knife knife4;say_team 已切换：折叠刀"
alias "knife4" "ent_fire weapon_knife changesubclass 506; alias knife knife5;say_team 已切换：穿肠刀"
alias "knife5" "ent_fire weapon_knife changesubclass 507; alias knife knife6;say_team 已切换：爪子刀"
alias "knife6" "ent_fire weapon_knife changesubclass 508; alias knife knife7;say_team 已切换：M9刺刀"
alias "knife7" "ent_fire weapon_knife changesubclass 509; alias knife knife8;say_team 已切换：猎杀者匕首"
alias "knife8" "ent_fire weapon_knife changesubclass 512; alias knife knife9;say_team 已切换：弯刀"
alias "knife9" "ent_fire weapon_knife changesubclass 514; alias knife knife10;say_team 已切换：鲍伊猎刀"
alias "knife10" "ent_fire weapon_knife changesubclass 515; alias knife knife11;say_team 已切换：蝴蝶刀"
alias "knife11" "ent_fire weapon_knife changesubclass 516; alias knife knife12;say_team 已切换：暗影双匕"
alias "knife12" "ent_fire weapon_knife changesubclass 517; alias knife knife13;say_team 已切换：系绳匕首"
alias "knife13" "ent_fire weapon_knife changesubclass 518; alias knife knife14;say_team 已切换：求生匕首"
alias "knife14" "ent_fire weapon_knife changesubclass 519; alias knife knife15;say_team 已切换：熊刀"
alias "knife15" "ent_fire weapon_knife changesubclass 520; alias knife knife16;say_team 已切换：折刀"
alias "knife16" "ent_fire weapon_knife changesubclass 521; alias knife knife17;say_team 已切换：流浪者匕首"
alias "knife17" "ent_fire weapon_knife changesubclass 522; alias knife knife18;say_team 已切换：短剑"
alias "knife18" "ent_fire weapon_knife changesubclass 523; alias knife knife19;say_team 已切换：锯齿爪刀"
alias "knife19" "ent_fire weapon_knife changesubclass 524; alias knife knife20;say_team 已切换：匕首"
alias "knife20" "ent_fire weapon_knife changesubclass 525; alias knife knife21;say_team 已切换：骷髅匕首"
alias "knife21" "ent_fire weapon_knife changesubclass 526; alias knife knife1;say_team 已切换：尼泊尔"
```

- “j”键启用，聊天框提示后，重新切刀即可。

## lastinv.cfg
- “弯刀”专用，规避了切刀时的双手拔刀动作，而是直接检视
```ini
unbind 1
unbind 2
unbind 3
unbind q
bind 1  eq_slot1
bind 2  eq_slot2
bind 3  eq_slot3
bind q  eq_lastinv
alias see "+lookatweapon;-lookatweapon"
alias eq_slot1    "slot1; set_slot1;"
alias eq_slot2    "slot2; set_slot2;"
alias eq_slot3    "slot3; set_slot3;see"
alias qs_slot1    "alias eq_invnext eq_slot2; alias eq_invprev eq_slot9; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot1; alias set_slot1 ; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot2    "alias eq_invnext eq_slot3; alias eq_invprev eq_slot1; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot2; alias set_slot1 qs_slot1; alias set_slot2 ; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot3    "alias eq_invnext eq_slot5; alias eq_invprev eq_slot2; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot3; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 ; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot5    "alias eq_invnext eq_slot6; alias eq_invprev eq_slot3; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot5; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 ; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot6    "alias eq_invnext eq_slot7; alias eq_invprev eq_slot5; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot6; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 ; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot7    "alias eq_invnext eq_slot8; alias eq_invprev eq_slot6; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot7; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 ; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot8    "alias eq_invnext eq_slot9; alias eq_invprev eq_slot7; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot8; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 ; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot9    "alias eq_invnext eq_slot1; alias eq_invprev eq_slot8; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot9; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 ; alias set_slot10 qs_slot10"
qs_slot2
eq_slot1
bind "." "unbind 1;unbind 2;unbind 3;unbind q;bind "1" "slot1";bind "2" "slot2";bind "3" "slot3";bind "q" "lastinv";say_team rebind!"
```

- “/”键启用，启用后“.”键取消该设置，与弯刀搭配使用，避免了切刀时的双手动作。

## zeus.cfg
- 电击枪快捷切换
```ini
alias "att0" "bind mouse1 +firr1;bind mouse2 +firr2"
alias "att1" "bind mouse1 +attack;bind mouse2 +attack2"
alias "+firr1" "+attack"
alias "-firr1" "-attack;slot2;slot1;att1;"
alias "+firr2" "+attack2"
alias "-firr2" "-attack2;slot2;slot1;att1;"
unbind 1
unbind 2
unbind 3
unbind 4
unbind 5
unbind q
bind "1" "slot1; att1"
bind "2" "slot2; att1"
bind "3" "slot3; att1"
bind "4" "slot11; att0"
bind "5" "slot5; att1"
bind "q" "lastinv; att1;"
```

- 在 autoexec.cfg 中自动启用，必须绑定“4”键电击枪，在电击枪左键使用之后自动切出主武器/副武器，手持电击枪右键时则不使用，直接切出主武器/副武器。

## crosshair_view.cfg
- 准星与持枪视角的存储与更换
```ini
say_team crosshair:"[",view:"]"
//default
cl_crosshair_drawoutline "false"
cl_crosshair_dynamic_maxdist_splitratio "0.300000"
cl_crosshair_dynamic_splitalpha_innermod "1.000000"
cl_crosshair_dynamic_splitalpha_outermod "0.500000"
cl_crosshair_dynamic_splitdist "7"
cl_crosshair_outlinethickness "1.000000"
cl_crosshair_recoil "false"
cl_crosshair_t "false"
cl_crosshairalpha "255"
cl_crosshaircolor "5"
cl_crosshaircolor_b "255"
cl_crosshaircolor_g "255"
cl_crosshaircolor_r "255"
cl_crosshairdot "false"
cl_crosshairgap "-3.400000"
cl_crosshairgap_useweaponvalue "false"
cl_crosshairsize "0.900000"
cl_crosshairstyle "4"
cl_crosshairthickness "0.800000"
cl_crosshairusealpha "true"
cl_crosshair_sniper_width "2"
viewmodel_fov 68
viewmodel_offset_x 2
viewmodel_offset_y 2
viewmodel_offset_z -1
viewmodel_presetpos 0
//crosshair
bind "[" "C"
alias "C" "C00"
alias "C00" "cl_crosshair_drawoutline "false";cl_crosshair_dynamic_maxdist_splitratio "0.300000";cl_crosshair_dynamic_splitalpha_innermod "1.000000";cl_crosshair_dynamic_splitalpha_outermod "0.500000";cl_crosshair_dynamic_splitdist "7";cl_crosshair_outlinethickness "0.500000";cl_crosshair_recoil "false";cl_crosshair_t "false";cl_crosshairalpha "255";cl_crosshaircolor "5";say_team a_50%!;alias C C01"
alias "C01" "cl_crosshaircolor_b "255";cl_crosshaircolor_g "255";cl_crosshaircolor_r "0";cl_crosshairdot "false";cl_crosshairgap "-2.400000";cl_crosshairgap_useweaponvalue "false";cl_crosshairsize "1.100000";cl_crosshairstyle "4";cl_crosshairthickness "0.100000";cl_crosshairusealpha "true";say_team a_100%!;alias C C02"
alias "C02" "cl_crosshair_drawoutline "false";cl_crosshair_dynamic_maxdist_splitratio "0.300000";cl_crosshair_dynamic_splitalpha_innermod "1.000000";cl_crosshair_dynamic_splitalpha_outermod "0.500000";cl_crosshair_dynamic_splitdist "7";cl_crosshair_outlinethickness "1.000000";cl_crosshair_recoil "false";cl_crosshair_t "false";cl_crosshairalpha "255";cl_crosshaircolor "5";say_team b_50%!;alias C C03"
alias "C03" "cl_crosshaircolor_b "255";cl_crosshaircolor_g "255";cl_crosshaircolor_r "255";cl_crosshairdot "false";cl_crosshairgap "-3.300000";cl_crosshairgap_useweaponvalue "false";cl_crosshairsize "1.400000";cl_crosshairstyle "5";cl_crosshairthickness "0.000000";cl_crosshairusealpha "true";say_team b_100%!;alias C C04"
alias "C04" "cl_crosshair_drawoutline "false";cl_crosshair_dynamic_maxdist_splitratio "0.000000";cl_crosshair_dynamic_splitalpha_innermod "1.000000";cl_crosshair_dynamic_splitalpha_outermod "1.000000";cl_crosshair_dynamic_splitdist "3";cl_crosshair_outlinethickness "1.000000";cl_crosshair_recoil "false";cl_crosshair_t "false";cl_crosshairalpha "255";cl_crosshaircolor "1";say_team c_50%!;alias C C05"
alias "C05" "cl_crosshaircolor_b "255";cl_crosshaircolor_g "246";cl_crosshaircolor_r "205";cl_crosshairdot "false";cl_crosshairgap "-6.000000";cl_crosshairgap_useweaponvalue "false";cl_crosshairsize "1.000000";cl_crosshairstyle "2";cl_crosshairthickness "1.000000";cl_crosshairusealpha "true";say_team c_100%!;alias C C06"
alias "C06" "cl_crosshair_drawoutline "true";cl_crosshair_dynamic_maxdist_splitratio "0.000000";cl_crosshair_dynamic_splitalpha_innermod "1.000000";cl_crosshair_dynamic_splitalpha_outermod "0.300000";cl_crosshair_dynamic_splitdist "5";cl_crosshair_outlinethickness "1.000000";cl_crosshair_recoil "false";cl_crosshair_t "false";cl_crosshairalpha "255";cl_crosshaircolor "2";say_team d_50%!;alias C C07"
alias "C07" "cl_crosshaircolor_b "0";cl_crosshaircolor_g "0";cl_crosshaircolor_r "0";cl_crosshairdot "true";cl_crosshairgap "-4.000000";cl_crosshairgap_useweaponvalue "false";cl_crosshairsize "0.500000";cl_crosshairstyle "4";cl_crosshairthickness "1.000000";cl_crosshairusealpha "true";say_team d_100%!;alias C C00"
//view
bind "]" "V"
alias "V" "V00"
alias "V00" "viewmodel_fov 60; viewmodel_offset_x 0; viewmodel_offset_y 1; viewmodel_offset_z -2; viewmodel_presetpos 0;say_team v_1!;alias V V01"
alias "V01" "viewmodel_fov 68; viewmodel_offset_x 2.5; viewmodel_offset_y -1; viewmodel_offset_z -2; viewmodel_presetpos 0;say_team v_2!;alias V V02"
alias "V02" "viewmodel_fov 68; viewmodel_offset_x 1.5; viewmodel_offset_y -2; viewmodel_offset_z -2; viewmodel_presetpos 0;say_team v_3!;alias V V00"
```

- "["或"]"键启用，"["键用于轮换准星设置，"]"键用于轮换持枪视角。
--- 

