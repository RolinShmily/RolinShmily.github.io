## _游戏自用 config 文件与部分指令分享_

### 一、cfg 功能简介

> - 自动加载文件，里面包含了一些键位设置，鼠标设置，和一键绑定，完整版放在最后

- **1. p** 键 开启自定义房间, **k** 键 掉刀, **l** 键 回看投掷物, **n** 键 开启飞行

```ini
sv_cheats 1; //开启作弊模式
bot_kick; //踢出机器人
mp_buy_anywhere 1; //可在任意处购买
mp_freezetime 0; //赛前准备时间为0
mp_maxmoney 99999; //最大金钱数99999
mp_startmoney 99999; //起始金钱数99999
mp_buytime 99999; //购买时间99999
mp_ignore_round_win_conditions 1; //回合永不结束
mp_respawn_on_death_ct 1; //ct无限复活
mp_respawn_on_death_t 1; //t无限复活
mp_friendlyfire 1; //队友伤害开启
ammo_grenade_limit_total 6; //手榴弹最大可携带数为6
mp_spectators_max 9; //游戏观察者最大数为9
mp_autokick 0;  //禁用自动踢出服务器功能
mp_restartgame 1; //在1s后重启回合
sv_grenade_trajectory_prac_pipreview 1; //启用手榴弹轨迹的预览
sv_grenade_trajectory_prac_trailtime 8; //设置手榴弹轨迹可见时间为8s
sv_infinite_ammo 2; //设置无限弹药模式(道具无限)，但仍需换弹夹
sv_showimpacts 1; //开启弹痕
say Practice Enabled;//全局喊话：练习模式
```

```ini
bind "p" "sv_cheats 1;bot_kick;mp_buy_anywhere 1;mp_freezetime 0;mp_maxmoney 99999;mp_startmoney 99999;mp_buytime 99999;mp_ignore_round_win_conditions 1; mp_respawn_on_death_ct 1;mp_respawn_on_death_t 1;mp_friendlyfire 1;ammo_grenade_limit_total 6;mp_spectators_max 9; mp_autokick 0; mp_restartgame 1;sv_grenade_trajectory_prac_pipreview 1; sv_grenade_trajectory_prac_trailtime 8;sv_infinite_ammo 2;sv_showimpacts 1;say Practice Enabled"
bind "k" "give weapon_knife"
bind "l" "sv_rethrow_last_grenade"
bind "n" "noclip"
```

- **2. j** 键对准刀具更换模型

```ini
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

- **3. 切出电击枪使用后快速自动切枪**

```ini
alias "att0" "bind mouse1 +firr1;bind mouse2 +firr2"
alias "att1" "bind mouse1 +attack;bind mouse2 +attack2"
alias "+firr1" "+attack"
alias "-firr1" "-attack;slot2;slot1;att1;"
alias "+firr2" "+attack2"
alias "-firr2" "-attack2;slot2;slot1;att1;"

bind "1" "slot1; att1" ; //主武器
bind "2" "slot2; att1" ; //副武器
bind "3" "slot3; att1" ; //近身武器
bind "4" "slot11; att0" ; //电击枪
bind "5" "slot5; att1" ; //C4
bind "q" "lastinv; att1;" ; //切换最近的武器装备
```

- **4. 基础绑定**

```ini
//键位
bind "w" "+forward"; //前进
bind "s" "+back"; //后退
bind "a" "+left"; //向左
bind "d" "+right"; //向右
bind "mouse1" "+attack"; //左键攻击
bind "mouse2" "+attack2"; //右键特殊攻击
bind "e" "+use"; //使用
bind "f" "+lookatweapon"; //检视
bind "space" "+jump" ; //跳跃
bind "ctrl" "+duck" ; //蹲下
bind "tab" "+showscores"; //打开计分板
bind "g" "drop" ; // 丢弃装备
bind "m" "teammenu"; //选择队伍
bind "shift" "+sprint"; //静步
bind "b" "buymenu" ;//购买菜单
bind "z" "slot6" ;//雷
bind "x" "slot3; slot7" ;//闪
bind "c" "slot8" ;//烟
bind "6" "slot9" ;//诱饵弹
bind "v" "slot10" ;//火
bind "i" "+spray_menu"; //打开涂鸦菜单
bind "u" "messagemode2";//团队聊天框
bind "y" "messagemode";//全局聊天框
bind "mouse4" "+voicerecord";//打开麦克风
bind "mouse5" "player_ping";//玩家标志
bind "mwheeldown" "+jump" ;//滚轮跳
bind "mwheelup" "+jump";//滚轮跳
bind "`" "toggleconsole";//打开控制台
bind "t" "switchhands";//切换左右手持枪
bind "h" "toggleradarscale"; //切换小地图缩放

bind "o" "exec autoexec.cfg";//加载自启动cfg
bind "\" "key_listboundkeys";//在控制台打印所有按键功能

bind "alt" "toggle cl_teamid_overhead_mode 1 3";//一键切换队友装备显示
bind "ralt" "radio2;slot12";//无线电与X光

bind "-" "toggle cl_draw_only_deathnotices 1 0";//UI开关
bind "=" "toggle cl_drawhud_force_radar 1 0";//雷达显示

```

- **5. 灵敏度、准星、持枪视角、雷达**

```ini
;//鼠标灵敏度
sensitivity 0.54
;//准星
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
;//圆圈准星
bind "[" "cl_crosshair_drawoutline "0";cl_crosshair_dynamic_maxdist_splitratio "0";cl_crosshair_dynamic_splitalpha_innermod "1";cl_crosshair_dynamic_splitalpha_outermod "0.5";cl_crosshair_dynamic_splitdist "7";cl_crosshair_friendly_warning "0";cl_crosshair_outlinethickness "0";cl_crosshair_sniper_show_normal_inaccuracy "0";cl_crosshair_t "0";cl_crosshairalpha "255";cl_crosshaircolor 5;cl_crosshaircolor_b "255";cl_crosshaircolor_g "255";cl_crosshaircolor_r "0";cl_crosshairdot "0";cl_crosshairgap "-3.9";cl_crosshairgap_useweaponvalue "0";cl_crosshairsize "0.9";cl_crosshairstyle "4";cl_crosshairthickness "1.5";cl_crosshairusealpha "1";"
;//狙击枪瞄准线宽度
cl_crosshair_sniper_width "2"
;//投掷物准星
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
;//持枪视角
viewmodel_fov 68
Viewmodel_offset_x 2.5
Viewmodel_offset_y -1
Viewmodel_offset_z -2
viewmodel_presetpos 3
;// "]"键超广角持枪
bind "]" "viewmodel_fov 68;viewmodel_offset_x 1.5;viewmodel_offset_y 2;viewmodel_offset_z -1;viewmodel_presetpos 3;"
;//雷达
cl_radar_always_centered "0"
cl_radar_scale "0.37"
cl_hud_radar_scale "1"
cl_teammate_colors_show 2
```

- **6. 杂项**

```ini
cl_hud_color "11";//HUD粉色
con_enable "1";//启用控制台
fps_max 0;//fps无上限
cl_join_advertise "2";//显示玩家计划加入反恐精英队
cl_use_opens_buy_menu "0"; //禁用在靠近购买区域时按下使用键（E键）自动打开购买菜单的功能
cl_dm_buyrandomweapons 0 ;//死亡竞技模式中禁用自动购买随机武器
gameinstructor_enable "0";//禁用游戏指导
cl_autohelp "false";//禁用自动帮助提示
mm_dedicated_search_maxping "70";//先选择延迟在 70 毫秒以内的服务器
func_break_max_pieces 0;//游戏会根据物体的属性生成默认数量的碎片
r_drawtracers_firstperson 1;//开启第一人称视角中的子弹轨迹
r_fullscreen_gamma 2.6;//调整游戏画面伽马值
cl_teamid_overhead_mode 3;//始终显示队友名称与装备
;//Ending
echo AutoConfig Enabled!;//控制台打印
say Hello!;//全局喊话
```

### 二、cfg 文件的位置和游戏自启动指令

> - 编辑好 cfg 文件要放入游戏文件夹对应位置才能生效
> - 相对路径：**.\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg**
> - 或者: **.\SteamLibrary\steamapps\common\Counter-Strike Global Offensive\game\csgo**

> - 在 steam 中的启动选项里可以方便设置一些东西：
> - **-allow_third_party_software** 允许第三方软件,例如**OBS**的窗口采集
> - **-perfectworld** 国服
> - **-worldwide** 国际服
> - 每条命令之间要留一个空格

### 三、一些好玩的指令

- **爆头模式**

```
mp_damage_headshot_only 1;
```

- **生成一只鸡**

```
ent_create chicken;
```

- **人机难度**

```
custom_bot_difficulty 5;
```

- **任意地点下包**

```
mp_plant_c4_anywhere 1;
```

- **C4 引爆时间**

```
mp_c4timer 40;
```

- **自动回血**

```
sv_regeneration_force_on 1;
```

- **显示人物行走速度**

```
cl_showpos 1;
```

- **武器掉落高亮**

```
mp_weapons_glow_on_ground 1;
```

### 四、autoexec.cfg

```ini
//tips01
alias "att0" "bind mouse1 +firr1;bind mouse2 +firr2"
alias "att1" "bind mouse1 +attack;bind mouse2 +attack2"

alias "+firr1" "+attack"
alias "-firr1" "-attack;slot2;slot1;att1;"
alias "+firr2" "+attack2"
alias "-firr2" "-attack2;slot2;slot1;att1;"

//Mouse
sensitivity 0.54

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
bind "1" "slot1; att1"
bind "2" "slot2; att1"
bind "3" "slot3; att1"
bind "4" "slot11; att0"
bind "5" "slot5; att1"

bind "z" "slot6"
bind "x" "slot3; slot7"
bind "c" "slot8"
bind "6" "slot9"
bind "v" "slot10"

bind "q" "lastinv; att1;"
bind "i" "+spray_menu"
bind "u" "messagemode2"
bind "y" "messagemode"
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
//cfg
bind "o" "exec autoexec.cfg;say auto!"
bind "\" "key_listboundkeys;say keys_log!"
bind "j" "exec knife.cfg;say knife_model!"
bind "p" "exec train.cfg;say train_model!"
bind "[" "exec crosshair_view;say crosshair_view!"
bind "]" "exec crosshair_view;say crosshair_view!"

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
Viewmodel_offset_y -1
Viewmodel_offset_z -2
viewmodel_presetpos 3

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
r_fullscreen_gamma 2.6
cl_use_opens_buy_menu false
cl_teamid_overhead_mode 3

//Ending
echo AutoConfig Enabled!
```

### 五、knife.cfg

```ini
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

### 六、crosshair_view.cfg

```ini
say niko_PI:"[",nanyi:"]"
//niko_PI
bind "[" "PI"
alias "PI" "PI00"

alias "PI00" "cl_crosshair_drawoutline "0";cl_crosshair_dynamic_maxdist_splitratio "0";cl_crosshair_dynamic_splitalpha_innermod "1";cl_crosshair_dynamic_splitalpha_outermod "0.5";cl_crosshair_dynamic_splitdist "7";cl_crosshair_friendly_warning "0";cl_crosshair_outlinethickness "0";cl_crosshair_sniper_show_normal_inaccuracy "0";alias PI PI01;say niko_PI_01/02!"

alias "PI01" "cl_crosshair_t "0";cl_crosshairalpha "255";cl_crosshaircolor 5;cl_crosshaircolor_b "255";cl_crosshaircolor_g "255";cl_crosshaircolor_r "0";cl_crosshairdot "0";cl_crosshairgap "-3.9";cl_crosshairgap_useweaponvalue "0";cl_crosshairsize "0.9";cl_crosshairstyle "4";cl_crosshairthickness "1.5";cl_crosshairusealpha "1";alias PI PI00;say niko_PI_02/02!"

//guangjiao
bind "]" "p"
alias "p" "p01"

alias "p01" "viewmodel_fov 68;viewmodel_offset_x 1.5;viewmodel_offset_y 2;viewmodel_offset_z -1;viewmodel_presetpos 3;say guangjiao!"
```

### 七、train.cfg

```ini
//Train
bind "k" "give weapon_knife"
bind "l" "sv_rethrow_last_grenade"
bind "n" "noclip"
bind "p" "sv_cheats 1;bot_kick;mp_buy_anywhere 1;mp_freezetime 0;mp_maxmoney 99999;mp_startmoney 99999;mp_buytime 99999;mp_ignore_round_win_conditions 1; mp_respawn_on_death_ct 1;mp_respawn_on_death_t 1;mp_friendlyfire 1;ammo_grenade_limit_total 6;mp_spectators_max 9; mp_autokick 0; mp_restartgame 1;sv_grenade_trajectory_prac_pipreview 1; sv_grenade_trajectory_prac_trailtime 8;sv_infinite_ammo 2;sv_showimpacts 1;say Practice Enabled"
```
