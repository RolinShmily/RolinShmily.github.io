## *游戏自用config文件与部分指令分享*
### *一、autoexec.cfg*
>- 自动加载文件，里面包含了一些键位设置，鼠标设置，和一键绑定
```ini
//Shubiao
sensitivity 1.25

//Jichu Bangding
bind "0" "slot10"
bind "1" "slot1"
bind "2" "slot2"
bind "3" "slot3"
bind "4" "slot4"
bind "5" "slot5"
bind "6" "slot6"
bind "7" "slot7"
bind "8" "slot8"
bind "9" "slot9"
bind "a" "+left" 
bind "d" "+right" 
bind "w" "+forward" 
bind "s" "+back"
bind "mouse1" "+attack" 
bind "mouse2" "+attack2" 
bind "e" "+use" 
bind "f" "+lookatweapon" 
bind "space" "+jump" 
bind "ctrl" "+duck" 
bind "g" "drop" 
bind shift "+sprint" 
bind "b" "buymenu" 

//Bangding
bind "n" "noclip" 
bind "c" "+voicerecord" 
bind "h" "toggleradarscale"
bind "v" "switchhands"

bind "[" "exec wdv3.cfg"
bind "]" "exec autoexec.cfg"

bind "i" "exec jiting.cfg"

bind "o" "exec huandao.cfg"

bind "\" "exec j.cfg"

bind "-" "cl_drawhud 0"
bind "=" "cl_drawhud 1"

bind "," "sv_showimpacts 1"
bind "." "sv_showimpacts 0"

bind "q" "lastinv"
bind "t" "+spray_menu"
bind "u" "messagemode2"
bind "y" "messagemode"
bind "z" "radio"
bind "MOUSE4" "+radialradio"
bind "MOUSE5" "player_ping"

bind "p" "sv_cheats 1;bot_kick;mp_buy_anywhere 1;mp_freezetime 0;mp_maxmoney 99999;mp_startmoney 99999; mp_buytime 99999;mp_ignore_round_win_conditions 1;mp_respawn_on_death_ct 1;mp_respawn_on_death_t 1;mp_autoteambalance 0;mp_friendlyfire 1;mp_solid_teammates 1;mp_taser_recharge_time 10;mp_drop_knife_enable true;ammo_grenade_limit_total 6;mp_spectators_max 9;mp_autokick 0;mp_limitteams 10;mp_restartgame 1;"
bind "/" "sv_grenade_trajectory_prac_pipreview 1;sv_grenade_trajectory_prac_trailtime 8;sv_infinite_ammo 2;"

bind "l" "sv_rethrow_last_grenade"
bind "j" "mp_restartgame 1"
bind "k" "give weapon_knife"


//Zhunxing
cl_crosshair_drawoutline false;
cl_crosshair_dynamic_maxdist_splitratio	0.300000;
cl_crosshair_dynamic_splitalpha_innermod 1.000000;
cl_crosshair_dynamic_splitalpha_outermod 0.500000;
cl_crosshair_dynamic_splitdist 7;
cl_crosshair_outlinethickness 0.000000;
cl_crosshair_recoil false;
cl_crosshair_sniper_width 1;
cl_crosshair_t false;
cl_crosshairalpha 255;
cl_crosshaircolor 5;
cl_crosshaircolor_b	255;
cl_crosshaircolor_g	255;
cl_crosshaircolor_r	0;
cl_crosshairdot	true;
cl_crosshairgap	-3.700000;
cl_crosshairgap_useweaponvalue false;
cl_crosshairsize 0.900000;
cl_crosshairstyle 5;
cl_crosshairthickness 0.800000;
cl_crosshairusealpha true;


//Chiqiang
viewmodel_fov "68.000000"
viewmodel_offset_x "2.0"
viewmodel_offset_y "2.0"
viewmodel_offset_z "-1.0"

//Leida
cl_radar_always_centered "0"
cl_radar_scale "0.37"
cl_hud_radar_scale "1"
cl_teammate_colors_show 2

//Qita
fps_max 999 
cl_join_advertise "2"
cl_use_opens_buy_menu "0" 
cl_dm_buyrandomweapons 0 
gameinstructor_enable "0"
cl_autohelp "false"
mm_dedicated_search_maxping "70" 
func_break_max_pieces 0
r_drawtracers_firstperson 0


echo Config Loaded!
```

>- **n** 键 飞天
>- **c** 键 讲话
>- **h** 键 切换小地图缩放比例
>- **v** 键 切换左右手
>- **z** 键 开启无线电
>- **t** 键 开启喷漆
>- **u** 键 团队消息
>- **y** 键 全体消息
>- **Mouth4** (侧键1) 快捷信息
>- **Mouth5** (侧键2) 玩家信号

- **p** 键 开启自定义房间：
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
mp_autoteambalance 0; //队伍平衡关闭
mp_friendlyfire 1; //队友伤害开启
mp_solid_teammates 1; //队友实体开启
mp_taser_recharge_time 10; //电击枪充电时间为10s
mp_drop_knife_enable true; //允许掉落匕首
ammo_grenade_limit_total 6; //手榴弹最大可携带数为6
mp_spectators_max 9; //游戏观察者最大数为9
mp_autokick 0; //禁用自动踢出服务器功能
mp_limitteams 10; //队伍间最大人数差为10
mp_restartgame 1; //在1s后重启回合
```
- **/** 键 开启道具可视化：
```ini
sv_grenade_trajectory_prac_pipreview 1; //启用手榴弹轨迹的预览
sv_grenade_trajectory_prac_trailtime 8; //设置手榴弹轨迹可见时间为8s
sv_infinite_ammo 2; //设置无限弹药模式(道具无限)，但仍需换弹夹
```
>- **l** 键 复现最后一次投掷的手榴弹
>- **j** 键 重启回合

>- **,** 键 开启弹痕
>- **.** 键 关闭弹痕

>- **-** 键 隐藏UI
>- **=** 键 开启UI

>- **k** 键 掉落一把匕首
- **o** 键 开启换刀 (**huandao.cfg**) 对准匕首即可
- **i** 键 开启急停模式，具体见**jiting.cfg**
- **\\** 键 开启彩虹hud，祥见**j.cfg** 
- **[** 键 启动弯刀自适应检视 (**wdv3.cfg**) 切刀按"**3**"触发
- **]** 键 重启**autoexec.cfg**文件，可以消除外置cfg文件的生效
### *二、cfg文件的位置和游戏自启动指令*
>- 编辑好cfg文件要放入游戏文件夹对应位置才能生效
>- 相对路径：**.\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg**

>- 在steam中的启动选项里可以方便设置一些东西：
>- **-allow_third_party_software** 允许第三方软件,例如**OBS**的窗口采集
>- **-perfectworld** 国服
>- **-worldwide** 国际服
>- 每条命令之间要留一个空格
### *三、huandao.cfg*
>- 更改匕首模型，对准匕首按 **o** 键即可
```ini
bind "o" "dao"                                                    
alias "dao" "dao1"
alias "dao1" "subclass_change 500; alias dao dao2"
alias "dao2" "subclass_change 503; alias dao dao3"
alias "dao3" "subclass_change 505; alias dao dao4"
alias "dao4" "subclass_change 506; alias dao dao5"
alias "dao5" "subclass_change 507; alias dao dao6"
alias "dao6" "subclass_change 508; alias dao dao7"
alias "dao7" "subclass_change 509; alias dao dao8"
alias "dao8" "subclass_change 512; alias dao dao9"
alias "dao9" "subclass_change 514; alias dao dao10"
alias "dao10" "subclass_change 515; alias dao dao11"
alias "dao11" "subclass_change 516; alias dao dao12"
alias "dao12" "subclass_change 517; alias dao dao13"
alias "dao13" "subclass_change 518; alias dao dao14"
alias "dao14" "subclass_change 519; alias dao dao15"
alias "dao15" "subclass_change 520; alias dao dao16"
alias "dao16" "subclass_change 521; alias dao dao17"
alias "dao17" "subclass_change 522; alias dao dao18"
alias "dao18" "subclass_change 523; alias dao dao19"
alias "dao19" "subclass_change 524; alias dao dao20"
alias "dao20" "subclass_change 524; alias dao dao21"
alias "dao21" "subclass_change 525; alias dao dao1"
alias "dao22" "subclass_change 526; alias dao dao1"
```
### *四、jiting.cfg*
>- cfg生效后，默认使用valorant版急停，长按空格键左侧的 **alt** 键切换 **双键劲舞团急停** 松开取消，按 **CapsLock** 键，切换valorant和双键急停，当然在autocfg下，按 **]** 键可恢复成原版急停，三种急停对比： ***BV12841167nH***
```ini
alias "+_forward" "+forward; forwardback 0.0001 0 0";
alias "-_forward" "-forward; forwardback -0.0001 0 0;rightleft 0 0 0";

alias "+_back" "+back; forwardback -0.0001 0 0";
alias "-_back" "-back; forwardback 0.0001 0 0;rightleft 0 0 0";

alias "+_left" "+left; rightleft -0.0001 0 0";
alias "-_left" "-left; rightleft 0.0001 0 0;forwardback 0 0 0";


alias "+_right" "+right; rightleft 0.0001 0 0";
alias "-_right" "-right; rightleft -0.0001 0 0;forwardback 0 0 0";

alias "+_forward1" "+forward; forwardback 0.0001 0 0";
alias "-_forward1" "-forward; forwardback 0 0 0";

alias "+_back1" "+back; forwardback -0.0001 0 0";
alias "-_back1" "-back; forwardback 0 0 0";

alias "+_left1" "+left; rightleft -0.0001 0 0";
alias "-_left1" "-left; rightleft 0 0 0";

alias "+_right1" "+right; rightleft 0.0001 0 0";
alias "-_right1" "-right; rightleft 0 0 0";

alias "+xjt" "bind "w" "+_forward";bind "s" "+_back";bind "a" "+_left";bind "d" "+_right";";
alias "+ljt" "bind "w" "+_forward1";bind "s" "+_back1";bind "a" "+_left1";bind "d" "+_right1";";

alias "+jt" "+ljt";
alias "-jt" "+xjt";
alias "+jt1" "+xjt";
alias "-jt1" "+ljt";
bind alt "+jt";
bind CAPSLOCK "+Ljt";

bind "w" "+_forward";
bind "s" "+_back";
bind "a" "+_left";
bind "d" "+_right"
```
### *五、j.cfg*
>- 方向键,切刀键和鼠标点击均会启动hud颜色循环
```ini
alias "+_forward" "+forward;cl_hud_color 11";
alias "-_forward" "-forward;cl_hud_color 8";
bind "w" "+_forward";
alias "+_back" "+back;cl_hud_color 9";
alias "-_back" "-back;cl_hud_color 10";
bind "s" "+_back";
alias "+_left" "+left;cl_hud_color 8";
alias "-_left" "-left;cl_hud_color 9";
bind "a" "+_left";
alias "+_right" "+right;cl_hud_color 10";
alias "-_right" "-right;cl_hud_color 5";
bind "d" "+_right";
bind "q" "lastinv;cl_hud_color 6"
alias +att"+attack;cl_hud_color 5;cl_crosshaircolor 7";
alias -att"-attack;cl_hud_color 9;cl_crosshaircolor 6";
bind mouse1"+att";
alias +att2"+attack2;cl_hud_color 2;cl_crosshaircolor 4;r_cleardecals";
```
### *六、wdv3.cfg*
>- 可忽略掉切出弯刀时的双手拿刀动作，而直接播放检视动画，转刀或者立刀
```ini
alias "q1" "lastinv"
alias "q2" weapon
alias "v1" "switchhands 1 0"
alias "v2" knifeswitch 

alias "view" "+lookatweapon;-lookatweapon"

alias "weapon" "lastinv;alias q2 knife;alias v2 gunswitch"
alias "knife" "lastinv;view;alias q2 weapon;alias v2 knifeswitch"
alias "knifeswitch" "switchhands 1 0;view"
alias "gunswitch" "switchhands 1 0"

bind "1" "slot1;bind q q1;bind v v1"
bind "2" "slot2;bind q q1;bind v v1"
bind "3" "slot3;view;bind q q2;alias q2 weapon;alias v2 knifeswitch;bind v v2"
bind "4" "slot4;bind q q1;bind v v1"
bind "5" "slot5;bind q q1;bind v v1"
bind "q" "q1"
bind "v" "v1"
```
### *七、一些好玩的指令*
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
- **C4引爆时间**
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