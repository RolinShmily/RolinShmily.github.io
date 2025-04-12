# 什么是CFG
**cfg** 是config(设置)的简写，可以理解为，拥有了cfg，你就拥有了在任何地点快速开一把cs的能力，不用再为设置而担忧。
## CFG存放位置
游戏全局cfg：
- 如果你的游戏存放盘符与steam存放盘符不同，就参考前者，若相同，则后者。

**...\SteamLibrary\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg** 或 **...\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg**
- 当然也可以在steam程序中寻找，下面是步骤。
1. 打开steam库，找到Counter-Strike 2，右击选择属性

![steam](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-12-52.webp)

2. 选择“已安装文件”，点击浏览

![steam2](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-14-48.webp)

3. 进入“game”，进入“csgo”，选择“cfg”，该目录下就是存放cfg文件的位置

![1](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-16-27.webp)

![2](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-18-03.webp)

![3](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-18-32.webp)

![4](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-19-00.webp)

个人用户cfg：
**...\Steam\userdata\123456789\730\local\cfg**
- 此处的“123456789”为steamID，可用于添加好友，如果你的PC上有多个steam账号登录过，那么在userdata文件夹中你会看到多个用户文件夹。
- 与游戏全局cfg不同，个人用户cfg的设置只用于该steam账号，并且多了一个 **cs2_video.txt** 配置文件,我倾向于只用这个video配置来同步画面设置，而绑定键位等用全局cfg。
## 如何创建一个cfg文件
1. 在桌面新建一个文本文档(也就是txt)，可以直接在这个txt文件中编写配置

![1](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-38-17.webp)

2. 编写完成后，在文件资源管理器中找到这个文件，更改后缀为cfg。
- 如果你无法显示后缀，按照下面操作

![2](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-12_23-41-02.webp)
## autoexec.cfg
这是一个只要你游戏启动就会自动加载的cfg，所以基础设置与按键绑定，可以直接写在这个cfg文件里。
- 下面给出一个模板，改写完成后要将文件名改为“autoexec.cfg”，并放在游戏全局cfg存放位置，才能生效。
```ini
#键位
bind "w" "+forward" #前进
bind "s" "+back" #后退
bind "a" "+left" #向左
bind "d" "+right" #向右
bind "mouse1" "+attack" #左键攻击
bind "mouse2" "+attack2" #右键特殊攻击
bind "e" "+use" #使用
bind "f" "+lookatweapon" #检视
bind "space" "+jump"  #跳跃
bind "ctrl" "+duck"  #蹲下
bind "tab" "+showscores" #打开计分板
bind "g" "drop"   #丢弃装备
bind "m" "teammenu" #选择队伍
bind "shift" "+sprint" #静步
bind "b" "buymenu" #购买菜单
bind "z" "slot6" #雷
bind "x" "slot7" #闪
bind "c" "slot8" #烟
bind "6" "slot9" #诱饵弹
bind "v" "slot10" #火
bind "y" "+spray_menu" #打开涂鸦菜单
bind "i" "messagemode2"#团队聊天框
bind "u" "messagemode"#全局聊天框
bind "mouse4" "+voicerecord"#打开麦克风
bind "mouse5" "player_ping"#玩家示意标志
bind "mwheeldown" "+jump" #滚轮下跳
bind "mwheelup" "+jump"#滚轮上跳
bind "`" "toggleconsole"#打开控制台
bind "t" "switchhands"#切换左右手持枪
bind "h" "toggleradarscale" #切换小地图缩放
bind "ralt" "radio2;slot12" #无线电与X光

#准星
cl_crosshair_drawoutline "0" # 禁用十字准星的轮廓线
cl_crosshair_dynamic_maxdist_splitratio "1" # 动态十字准星的最大分离距离比例
cl_crosshair_dynamic_splitalpha_innermod "0" # 动态十字准星内部分离部分的透明度
cl_crosshair_dynamic_splitalpha_outermod "1" # 动态十字准星外部分离部分的透明度
cl_crosshair_dynamic_splitdist "3" # 动态十字准星的分离距离
cl_crosshair_friendly_warning "0" # 禁用对友军的十字准星警告
cl_crosshair_outlinethickness "1" # 十字准星轮廓线的厚度
cl_crosshair_sniper_show_normal_inaccuracy "0" # 禁用狙击枪十字准星显示正常不准确度
cl_crosshair_t "0" # 禁用T形十字准星
cl_crosshairalpha "255" # 十字准星的透明度（255为完全不透明）
cl_crosshaircolor 5 # 设置十字准星颜色为自定义（5表示自定义颜色）
cl_crosshaircolor_b "255" # 自定义十字准星的蓝色分量（255为最大）
cl_crosshaircolor_g "255" # 自定义十字准星的绿色分量（255为最大）
cl_crosshaircolor_r "0" # 自定义十字准星的红色分量（0为最小）
cl_crosshairdot "0" # 禁用十字准星中心点
cl_crosshairgap "-3.644676" # 设置十字准星的间隙（负值表示向内收缩）
cl_crosshairgap_useweaponvalue "0" # 禁用根据武器值调整十字准星间隙
cl_crosshairsize "0.901125" # 设置十字准星的大小
cl_crosshairstyle "4" # 设置十字准星样式为经典静态（4表示经典静态）
cl_crosshairthickness "0.961664" # 设置十字准星的厚度
cl_crosshairusealpha "1" # 启用十字准星的透明度设置

#狙击枪瞄准线宽度
cl_crosshair_sniper_width "2"

#鼠标灵敏度
sensitivity 0.50

#持枪视角
viewmodel_fov 68 # 设置第一人称视角的视野范围（FOV），值越大，视野越广
Viewmodel_offset_x 2.5 # 调整武器模型在水平方向（X轴）上的偏移，正值向右，负值向左
Viewmodel_offset_y 0 # 调整武器模型在垂直方向（Y轴）上的偏移，正值向上，负值向下
Viewmodel_offset_z -1.5 # 调整武器模型在深度方向（Z轴）上的偏移，正值向前，负值向后
viewmodel_presetpos 2 # 使用预设的武器模型位置（2表示经典位置）

#雷达
cl_radar_always_centered "0" # 禁用雷达始终以玩家为中心，雷达会显示地图的完整区域
cl_radar_scale "0.37" # 设置雷达的缩放比例，值越小，雷达显示的范围越大
cl_hud_radar_scale "1" # 设置HUD上雷达的缩放比例，1为默认大小
cl_teammate_colors_show 2 # 设置队友颜色显示模式，2表示显示队友的轮廓颜色
```
## cs2_video.txt
同步画面设置
- 给出模板
```ini
"video.cfg"
{
	"Version"		"15" # 配置文件版本号
	"VendorID"		"4318" # 显卡厂商 ID（例如 NVIDIA、AMD）
	"DeviceID"		"10464" # 显卡设备 ID
	"setting.cpu_level"		"3" # CPU 性能等级（0-3，3 为最高）
	"setting.gpu_mem_level"		"3" # GPU 显存性能等级（0-3，3 为最高）
	"setting.gpu_level"		"3" # GPU 性能等级（0-3，3 为最高）
	"setting.knowndevice"		"0" # 是否识别为已知设备（0 为否，1 为是）
	"setting.defaultres"		"1920" # 默认分辨率宽度（1920x1080）
	"setting.defaultresheight"		"1080" # 默认分辨率高度（1920x1080）
	"setting.refreshrate_numerator"		"0" # 刷新率分子（0 表示使用默认值）
	"setting.refreshrate_denominator"		"0" # 刷新率分母（0 表示使用默认值）
	"setting.fullscreen"		"1" # 是否启用全屏模式（0 为否，1 为是）
	"setting.coop_fullscreen"		"1" # 合作模式是否启用全屏（1 为是）
	"setting.nowindowborder"		"1" # 是否启用无边框窗口模式（1 为是）
	"setting.mat_vsync"		"0" # 是否启用垂直同步（0 为否，1 为是）
	"setting.fullscreen_min_on_focus_loss"		"0" # 失去焦点时是否最小化全屏窗口（0 为否）
	"setting.high_dpi"		"0" # 是否启用高 DPI 缩放（0 为否）
	"AutoConfig"		"2" # 自动配置等级（2 为自定义配置）
	"setting.shaderquality"		"0" # 着色器质量（0 为低，1 为中，2 为高）
	"setting.r_texturefilteringquality"		"3" # 纹理过滤质量（0-3，3 为最高）
	"setting.msaa_samples"		"4" # 多重采样抗锯齿（MSAA）采样数（4 为 4x MSAA）
	"setting.r_csgo_cmaa_enable"		"0" # 是否启用 CMAA 抗锯齿（0 为否）
	"setting.videocfg_shadow_quality"		"2" # 阴影质量（0 为低，1 为中，2 为高）
	"setting.videocfg_dynamic_shadows"		"1" # 是否启用动态阴影（1 为是）
	"setting.videocfg_texture_detail"		"2" # 纹理细节（0 为低，1 为中，2 为高）
	"setting.videocfg_particle_detail"		"2" # 粒子细节（0 为低，1 为中，2 为高）
	"setting.videocfg_ao_detail"		"2" # 环境光遮蔽（AO）细节（0 为低，1 为中，2 为高）
	"setting.videocfg_hdr_detail"		"3" # HDR 细节（0-3，3 为最高）
	"setting.videocfg_fsr_detail"		"0" # FSR（FidelityFX Super Resolution）细节（0 为禁用）
	"setting.monitor_index"		"0" # 显示器索引（0 为主显示器）
	"setting.r_low_latency"		"1" # 是否启用低延迟模式（1 为是）
	"setting.aspectratiomode"		"0" # 宽高比模式（0 为自动，1 为 4:3，2 为 16:9）
}
```
# 设置启动项
- 启动项设置位置：在steam库中选择CS2属性，选择“通用”，在下方黑框内填写。

![qidong](https://cdn.jsdelivr.net/gh/RolinShmily/Images@main/PixPin_2025-04-13_00-11-22.webp)

- 下面使一些常用启动项，需要注意的是，每一条指令之间要有一个空格。
```ini
-novid  #关闭过场动画
-high  #提高CSGO程序优先级，有可能负优化
-nojoy #关闭手柄相关，降低内存占用
-perfectworld  #直接进入国服
-worldwide  #直接进入国际服
-w 1920 -h 1080  #设置分辨率1920x1080
+exec auto.cfg  #加载auto.cfg
+fps_max 300  #限制fps最大300
-allow_third_party_software  #允许OBS等第三方软件
-noreflex #取消游戏内的reflex功能，可以在NVIDIA控制面板中开启
```

# 控制台指令
 了解控制台指令功能，可以将其绑定在按键上，并写入cfg文件，快速实现功能。
- 下面给出亿些指令
```ini
sv_cheats 1 # 开启作弊模式，允许使用作弊命令
bot_kick # 踢出所有机器人
mp_buy_anywhere 1 # 允许在任意位置购买装备
mp_freezetime 0 # 设置赛前准备时间为0秒
mp_maxmoney 99999 # 设置最大金钱数为99999
mp_startmoney 99999 # 设置起始金钱数为99999
mp_buytime 99999 # 设置购买时间为99999秒
mp_ignore_round_win_conditions 1 # 回合永不结束
mp_respawn_on_death_ct 1 # CT阵营无限复活
mp_respawn_on_death_t 1 # T阵营无限复活
mp_friendlyfire 1 # 开启队友伤害
ammo_grenade_limit_total 6 # 设置手榴弹最大可携带数为6
mp_spectators_max 9 # 设置游戏观察者最大数为9
mp_autokick 0 # 禁用自动踢出服务器功能
mp_restartgame 1 # 在1秒后重启回合
sv_grenade_trajectory_prac_pipreview 1 # 启用手榴弹轨迹的预览
sv_grenade_trajectory_prac_trailtime 8 # 设置手榴弹轨迹可见时间为8秒
sv_infinite_ammo 2 # 设置无限弹药模式（道具无限），但仍需换弹夹
sv_showimpacts 1 # 开启弹痕显示

exec autoexec.cfg # 执行 autoexec.cfg 配置文件，加载自定义设置
key_listboundkeys # 列出所有已绑定的按键及其对应的命令
toggle cl_teamid_overhead_mode 1 3 # 切换队友头顶标识模式（1 为简单标识，3 为详细标识）
toggle cl_draw_only_deathnotices 1 0 # 切换是否仅显示死亡通知（1 为仅显示，0 为显示完整 HUD）
toggle cl_drawhud_force_radar 1 0 # 切换是否强制显示雷达（1 为强制显示，0 为正常显示）

cl_hud_color "11" # 设置 HUD 颜色为粉色
con_enable "1" # 启用控制台功能
fps_max 0 # 设置 FPS 无上限，允许游戏以最高帧率运行
cl_join_advertise "2" # 显示玩家计划加入反恐精英队的信息
cl_use_opens_buy_menu "0" # 禁用在靠近购买区域时按下使用键（E键）自动打开购买菜单的功能
cl_dm_buyrandomweapons 0 # 在死亡竞技模式中禁用自动购买随机武器
gameinstructor_enable "0" # 禁用游戏指导功能
cl_autohelp "false" # 禁用自动帮助提示
mm_dedicated_search_maxping "70" # 优先选择延迟在 70 毫秒以内的服务器
func_break_max_pieces 0 # 游戏会根据物体的属性生成默认数量的碎片
r_drawtracers_firstperson 1 # 开启第一人称视角中的子弹轨迹显示
r_fullscreen_gamma 3.0 # 调整游戏画面伽马值为 3.0
cl_teamid_overhead_mode 3 # 始终显示队友名称与装备信息
echo AutoConfig Enabled! # 在控制台打印 "AutoConfig Enabled!" 提示信息

mp_damage_headshot_only 1 # 仅爆头才能造成伤害，其他部位攻击无效
ent_create chicken # 在游戏中生成一只鸡（娱乐功能）
custom_bot_difficulty 5 # 设置自定义 BOT 难度为最高（5 为最高难度）
mp_plant_c4_anywhere 1 # 允许在任何位置安放 C4 炸弹
mp_c4timer 40 # 设置 C4 炸弹的倒计时为 40 秒
sv_regeneration_force_on 1 # 开启生命值自动回复功能
cl_showpos 1 # 在屏幕上显示玩家当前的位置、速度和角度信息
mp_weapons_glow_on_ground 1 # 开启地面武器的高亮显示功能
```

# 自用配置分享
## 启动项
```
-allow_third_party_software -noreflex -high -w 1920 -h 1440
```
## cs2_video.txt
```
"video.cfg"
{
	"Version"		"15"
	"VendorID"		"4318"
	"DeviceID"		"10464"
	"setting.cpu_level"		"3"
	"setting.gpu_mem_level"		"3"
	"setting.gpu_level"		"3"
	"setting.knowndevice"		"0"
	"setting.defaultres"		"1920"
	"setting.defaultresheight"		"1440"
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
## autoexec.cfg
```
//Mouse
sensitivity 0.50

//Keys
bind "w" "+forward"
bind "s" "+back"
bind "a" "+left"
bind "d" "+right"
bind "mouse1" "+attack" 
bind "mouse2" "+attack2"
bind "e" "+use"
bind "f" "+lookatweapon"
bind "space" "+jump" 
bind "ctrl" "+duck" 
bind "tab" "+showscores"
bind "g" "drop" 
bind "m" "teammenu"
bind "shift" "+sprint" 
bind "b" "buymenu" 
bind "1" "slot1" 
bind "2" "slot2"  
bind "3" "slot3" 
bind "4" "slot11" 
bind "5" "slot5"

bind "z" "slot6;" 
bind "x" "slot7" 
bind "c" "slot8" 
bind "6" "slot9" 
bind "v" "slot10" 

bind "q" "lastinv"
bind "y" "+spray_menu"
bind "i" "messagemode2"
bind "u" "messagemode"
bind "mouse4" "+voicerecord"
bind "mouse5" "player_ping"
bind "mwheeldown" "+jump" 
bind "mwheelup" "+jump"
bind "`" "toggleconsole"

bind "t" "switchhands"
bind "h" "toggleradarscale" 

bind "alt" "toggle cl_teamid_overhead_mode 1 3"
bind "ralt" "radio2;slot12"

bind "-" "toggle cl_draw_only_deathnotices 1 0"
bind "=" "toggle cl_drawhud_force_radar 1 0"

bind "f5" "buy hegrenade"
bind "f6" "buy flashbang"
bind "f7" "buy smokegrenade"
bind "f8" "buy molotov;buy incgrenade"
bind "f9" "buy vest"
bind "f10" "buy vesthelm"
bind "f11" "buy defuser"
bind "f4" "buy rifle1"
bind "f3" "buy secondary4"
bind "f12" "sellbackall"

//cfg
exec zeus.cfg
bind "o" "exec autoexec.cfg;say auto!"
bind "." "exec rebind.cfg:say rebind!"
bind "\" "key_listboundkeys;say keys_log!"
bind "j" "exec knife.cfg;say knife_model!"
bind "p" "exec train.cfg;say train_model!"
bind "[" "exec crosshair_view;say crosshair_view!"
bind "]" "exec crosshair_view;say crosshair_view!"
bind "/" "exec lastinv.cfg;say lastinv!"

//Crosshair
cl_crosshair_drawoutline "0"
cl_crosshair_dynamic_maxdist_splitratio "1"
cl_crosshair_dynamic_splitalpha_innermod "0"
cl_crosshair_dynamic_splitalpha_outermod "1"
cl_crosshair_dynamic_splitdist "3"
cl_crosshair_friendly_warning "0"
cl_crosshair_outlinethickness "1"
cl_crosshair_sniper_show_normal_inaccuracy "0"
cl_crosshair_t "0"
cl_crosshairalpha "255"
cl_crosshaircolor 5
cl_crosshaircolor_b "255"
cl_crosshaircolor_g "255"
cl_crosshaircolor_r "0"
cl_crosshairdot "0"
cl_crosshairgap "-3.644676"
cl_crosshairgap_useweaponvalue "0"
cl_crosshairsize "0.901125"
cl_crosshairstyle "4"
cl_crosshairthickness "0.961664"
cl_crosshairusealpha "1"

//sniper_crosshair
cl_crosshair_sniper_width "2"

//more_crosshair
cl_fixedcrosshaigap "3"
cl_grenadecrosshair_decoy 1
cl_grenadecrosshair_explosive 1
cl_grenadecrosshair_fire 1
cl_grenadecrosshair_flash 1
cl_grenadecrosshair_keepusercrosshair 1
cl_grenadecrosshair_smoke 1
cl_grenadecrosshairdelay_decoy "0.114345"
cl_grenadecrosshairdelay_explosive "0.114345"
cl_grenadecrosshairdelay_fire "0.114345"
cl_grenadecrosshairdelay_flash "0.114345"
cl_grenadecrosshairdelay_smoke "0.114345"
cl_observed_bot_crosshair 2
cl_show_observer_crosshair 2
cl_teamid_overhead_fade_near_crosshair "0.5"

//Gun's view
viewmodel_fov 68
Viewmodel_offset_x 2.5
Viewmodel_offset_y 0
Viewmodel_offset_z -1.5
viewmodel_presetpos 2

//Radar
cl_radar_always_centered "0"
cl_radar_scale "0.37"
cl_hud_radar_scale "1"
cl_teammate_colors_show 2

//Others
cl_hud_color "11"
con_enable "1"
fps_max 0
cl_join_advertise "2"
cl_use_opens_buy_menu "0" 
cl_dm_buyrandomweapons 0 
gameinstructor_enable "0"
cl_autohelp "false"
mm_dedicated_search_maxping "70"
func_break_max_pieces 0
r_drawtracers_firstperson 1
r_fullscreen_gamma 3.0
cl_use_opens_buy_menu false
cl_teamid_overhead_mode 3

//Ending
echo AutoConfig Enabled!
```
## train.cfg
```
//Train
bind "k" "sv_cheats 1;give weapon_knife"
bind "l" "sv_rethrow_last_grenade"
bind "n" "noclip"
bind "p" "sv_cheats 1;bot_kick;mp_buy_anywhere 1;mp_freezetime 0;mp_maxmoney 99999;mp_startmoney 99999;mp_buytime 99999;mp_ignore_round_win_conditions 1; mp_respawn_on_death_ct 1;mp_respawn_on_death_t 1;mp_friendlyfire 1;ammo_grenade_limit_total 6;mp_spectators_max 9; mp_autokick 0; mp_restartgame 1;sv_grenade_trajectory_prac_pipreview 1; sv_grenade_trajectory_prac_trailtime 8;sv_infinite_ammo 2;sv_showimpacts 1;say Practice Enabled"
```
## knife.cfg
```
//knife_change
bind "j" "mp_drop_knife_enable 1;knife"                                                    
alias "knife" "knife1"
alias "knife1" "subclass_change 500; alias knife knife2"
alias "knife2" "subclass_change 503; alias knife knife3"
alias "knife3" "subclass_change 505; alias knife knife4"
alias "knife4" "subclass_change 506; alias knife knife5"
alias "knife5" "subclass_change 507; alias knife knife6"
alias "knife6" "subclass_change 508; alias knife knife7"
alias "knife7" "subclass_change 509; alias knife knife8"
alias "knife8" "subclass_change 512; alias knife knife9"
alias "knife9" "subclass_change 514; alias knife knife10"
alias "knife10" "subclass_change 515; alias knife knife11"
alias "knife11" "subclass_change 516; alias knife knife12"
alias "knife12" "subclass_change 517; alias knife knife13"
alias "knife13" "subclass_change 518; alias knife knife14"
alias "knife14" "subclass_change 519; alias knife knife15"
alias "knife15" "subclass_change 520; alias knife knife16"
alias "knife16" "subclass_change 521; alias knife knife17"
alias "knife17" "subclass_change 522; alias knife knife18"
alias "knife18" "subclass_change 523; alias knife knife19"
alias "knife19" "subclass_change 524; alias knife knife20"
alias "knife20" "subclass_change 525; alias knife knife21"
alias "knife21" "subclass_change 526; alias knife knife1"
```
## lastinv.cfg
```
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
```
## zeus.cfg
```
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
## crosshair_view.cfg
```
say niko_PI:"[",nanyi:"]"
//niko_PI
bind "[" "PI"
alias "PI" "PI00"
alias "PI00" "cl_crosshair_drawoutline "0";cl_crosshair_dynamic_maxdist_splitratio "0";cl_crosshair_dynamic_splitalpha_innermod "1";cl_crosshair_dynamic_splitalpha_outermod "0.5";cl_crosshair_dynamic_splitdist "7";cl_crosshair_friendly_warning "0";cl_crosshair_outlinethickness "0";cl_crosshair_sniper_show_normal_inaccuracy "0";alias PI PI01;say niko_PI_01/02!"
alias "PI01" "cl_crosshair_t "0";cl_crosshairalpha "255";cl_crosshaircolor 5;cl_crosshaircolor_b "255";cl_crosshaircolor_g "255";cl_crosshaircolor_r "0";cl_crosshairdot "0";cl_crosshairgap "-3.9";cl_crosshairgap_useweaponvalue "0";cl_crosshairsize "0.9";cl_crosshairstyle "4";cl_crosshairthickness "1.5";cl_crosshairusealpha "1";alias PI PI00;say niko_PI_02/02!"
//nanyi
bind "]" "p"
alias "p" "p01"
alias "p01" "viewmodel_fov 68;viewmodel_offset_x 1.5;viewmodel_offset_y 2;viewmodel_offset_z -1;viewmodel_presetpos 3;say nanyi!"
```