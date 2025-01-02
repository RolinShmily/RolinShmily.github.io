## _游戏自用 config 文件与部分指令分享_

### 一、cfg 功能简介

> - 自动加载文件，里面包含了一些键位设置，鼠标设置，和一键绑定，完整版放在最后

- **1. p** 键 开启自定义房间, **k** 键 掉刀, **l** 键 回看投掷物, **n** 键 开启飞行
- 对应 **train.cfg**
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
bind "x" "slot7" ;//闪
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

- **4. 灵敏度、准星、持枪视角、雷达**

```ini
;//鼠标灵敏度
sensitivity 0.50
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
Viewmodel_offset_y 0
Viewmodel_offset_z -1.5
viewmodel_presetpos 2
;// "]"键超广角持枪
bind "]" "viewmodel_fov 68;viewmodel_offset_x 1.5;viewmodel_offset_y 2;viewmodel_offset_z -1;viewmodel_presetpos 3;"
;//雷达
cl_radar_always_centered "0"
cl_radar_scale "0.37"
cl_hud_radar_scale "1"
cl_teammate_colors_show 2
```

- **5. 杂项**

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
r_fullscreen_gamma 3.0;//调整游戏画面伽马值
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
exec zeus.cfg
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

### 八、zeus.cfg
- 电击枪使用后快速回收
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

### 九、lastinv.cfg

```ini
//Weapon viewmodel script for Launders. Based on a TF2 script by /u/genemilder (http://pastebin.com/7beau8BP). Modified for csgo by /u/Flapadiddle (http://steamcommunity.com/id/flapadiddle) 2014/12/29
 
//This script allows one to create individual settings for each inventory slot while preserving quickswitching functionality. There is also the option to use mouse scrolling if desired. Slot4 is excluded because the grenade cycle functionality is not compatiable with this logic.  
 
//Place this in your autoexec after verifiying that it works. You may have to remove existing binds to the keys that you use here to avoid complications.  
 
// ========== BINDS ==========
   //Bind whatever keys you like. next/previous inventory binds are commented by default, uncomment and add keys to enable.  
//根据国外牛人改编，适用于CS2
//代码功能是在按3切刀或者按Q切刀时自动检视，但在按Q切枪时不进行自动检视，弯刀用户狂喜
//解绑重置接下来需要自定义的键
unbind 1
unbind 2
unbind 3
//unbind 4
//unbind 5
unbind q

bind 1            eq_slot1   //绑定主武器按键
bind 2            eq_slot2  //绑定副武器按键
bind 3            eq_slot3  //绑定刀按键
bind q            eq_lastinv //快速切换上次使用的武器按键，这里重写了lastinv函数，即此时的 eq_lastinv，所以没用到官方的函数lastinv
//bind 4            eq_slot4
//bind 5            eq_slot5
//bind 6            eq_slot6
//bind 7            eq_slot7
//bind 8            eq_slot8
//bind 9            eq_slot9

//修复了滚轮切枪时Q不记忆的问题，即就算使用滚轮切枪，还是进行最后一次按键切枪的快速切枪操作， 但还有个BUG是4有烟火雷闪多个道具时不能切换，只能切换到道具中第一个，我的建议是滚轮切枪就不要自动检视了，不会吧真有人还用滚轮切枪（狗头保命）
//bind MWHEELDOWN      eq_invnext //选择下一个武器
//bind MWHEELUP      eq_invprev //选择上一个武器
 
// ========== SETTINGS ==========
  //insert any settings you wish to add for individual slots (xhair, viewmodel, sensitivity etc.) with a semicolon and the command. the example below puts only the knife in your left hand.
//按键功能配置映射

alias see "+lookatweapon;-lookatweapon"    //CS2最新检视命令
alias eq_slot1    "slot1; set_slot1;"
alias eq_slot2    "slot2; set_slot2;"  
alias eq_slot3    "slot3; set_slot3;see"   //只要切换到刀就会自动检视，无论是按3切刀还是按Q切刀
//alias eq_slot4    "slot4; set_slot4;"  
//alias eq_slot5    "slot5; set_slot5;"
//alias eq_slot6    "slot6; set_slot6;"
//alias eq_slot7    "slot7; set_slot7;"
//alias eq_slot8    "slot8; set_slot8;"
//alias eq_slot9    "slot9; set_slot9;"  
//alias eq_invprev "invprev"
//alias eq_invnext "invnext"

 
// ========== LOGIC ==========
  //No touching. Basically this manually implements quiswitching without the 'lastinv' command and next/previous inventory selection 
//下面的代码不要动，它可以不使用游戏自带的代码lastinv但能实现同样的切换上一把武器的效果，大概实现原理是每次按下一个键（假设是1）后会执行你按下的上一个键（假设是3）里面的set_lastinv函数，而每一个按键的set_lastinv函数都会覆盖重写，定义按下q时切换到当前按键的武器，即此时的下一个武器（就是先按3再按1后，set_lastinv函数还是指向3），从而实现切换上一个武器效果 
//关于这里为什么重写lastinv函数而不用游戏中自带的函数，我认为是为了在切换到上一个武器过程中添加自定义操作（检视刀并且不检视其他枪），官方的lastinv函数显然做不到这点

alias qs_slot1    "alias eq_invnext eq_slot2; alias eq_invprev eq_slot9; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot1; alias set_slot1 ; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot2    "alias eq_invnext eq_slot3; alias eq_invprev eq_slot1; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot2; alias set_slot1 qs_slot1; alias set_slot2 ; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot3    "alias eq_invnext eq_slot5; alias eq_invprev eq_slot2; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot3; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 ; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
//alias qs_slot4    "alias eq_invnext eq_slot5; alias eq_invprev eq_slot3; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot4; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3 ;alias set_slot4;  alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot5    "alias eq_invnext eq_slot6; alias eq_invprev eq_slot3; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot5; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 ; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot6    "alias eq_invnext eq_slot7; alias eq_invprev eq_slot5; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot6; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 ; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot7    "alias eq_invnext eq_slot8; alias eq_invprev eq_slot6; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot7; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 ; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"  
alias qs_slot8    "alias eq_invnext eq_slot9; alias eq_invprev eq_slot7; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot8; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 ; alias set_slot9 qs_slot9; alias set_slot10 qs_slot10"
alias qs_slot9    "alias eq_invnext eq_slot1; alias eq_invprev eq_slot8; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot9; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 ; alias set_slot10 qs_slot10"
//alias qs_slot10   "alias eq_invnext eq_slot1; alias eq_invprev eq_slot9; set_lastinv; alias set_lastinv alias eq_lastinv eq_slot10; alias set_slot1 qs_slot1; alias set_slot2 qs_slot2; alias set_slot3 qs_slot3; alias set_slot5 qs_slot5; alias set_slot6 qs_slot6; alias set_slot7 qs_slot7; alias set_slot8 qs_slot8; alias set_slot9 qs_slot9; alias set_slot10 "
 
//代码初始化
qs_slot2
eq_slot1
```