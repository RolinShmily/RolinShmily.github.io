## *游戏自用config文件*
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

bind "'" "exec nb.cfg"

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
- **'** 键 开启连喷模式，具体见**nb.cfg**
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
### *四、nb.cfg*
>- cfg生效后，按空格键右侧的 **alt** 键切换**hud**为**蓝色**和**黄色**两种模式，分别对应两套模板，在对应状态下按 **'** 键即可发送消息
```ini
alias "ez01" "say EZ;bind "'" "ez02"";
alias "ez02" "say 收徒;bind "'" "ez03"";
alias "ez03" "say 不收后三名;bind "'" "ez04"";
alias "ez04" "say 统一回复：没开;bind "'" "ez05"";
alias "ez05" "say 叫你家大人来打;bind "'" "ez06"";
alias "ez06" "say 有真人吗？;bind "'" "ez07"";
alias "ez07" "say 练枪图吗这是？;bind "'" "ez08"";
alias "ez08" "say 4399？;bind "'" "ez09"";
alias "ez09" "say 你的枪法比较松弛，但你匪夷所思的走位弥补了这一点;bind "'" "ez10"";
alias "ez10" "say 下课;bind "'" "ez11"";

alias "ez11" "say 开了吗？我说灵智;bind "'" "ez12"";
alias "ez12" "say 征婚;bind "'" "ez13"";
alias "ez13" "say 纳妾;bind "'" "ez14"";
alias "ez14" "say 领|养;bind "'" "ez15"";
alias "ez15" "say 假肢上门安装;bind "'" "ez16"";
alias "ez16" "say 正视差距;bind "'" "ez17"";
alias "ez17" "say 找不到投降吗？;bind "'" "ez18"";
alias "ez18" "say 投降在左上角;bind "'" "ez19"";
alias "ez19" "say 蝼|蚁;bind "'" "ez20"";
alias "ez20" "say 失望;bind "'" "ez21"";

alias "ez21" "say 自己找差距;bind "'" "ez22"";
alias "ez22" "say 不接单;bind "'" "ez23"";
alias "ez23" "say 小段60大段150;bind "'" "ez24"";
alias "ez24" "say 墨镜上车;bind "'" "ez25"";
alias "ez25" "say bot？;bind "'" "ez26"";
alias "ez26" "say 人机怎么加难度？;bind "'" "ez27"";
alias "ez27" "say 伒亲繁殖？;bind "'" "ez28"";
alias "ez28" "say 我匹的是新手教程？;bind "'" "ez29"";
alias "ez29" "say 已经很棒了;bind "'" "ez30"";
alias "ez30" "say 浪费我的网费;bind "'" "ez31"";

alias "ez31" "say 勤能补拙;bind "'" "ez32"";
alias "ez32" "say 来调灵敏度的;bind "'" "ez33"";
alias "ez33" "say 白练一把;bind "'" "ez34"";
alias "ez34" "say 来点强度;bind "'" "ez35"";
alias "ez35" "say 小号;bind "'" "ez36"";
alias "ez36" "say 不是本人，别加;bind "'" "ez37"";
alias "ez37" "say 下把记得晚点匹;bind "'" "ez38"";
alias "ez38" "say 元梦之星转来的;bind "'" "ez39"";
alias "ez39" "say 随便玩玩，不带妹;bind "'" "ez40"";
alias "ez40" "say 年轻人，未来是你们的;bind "'" "ez41"";

alias "ez41" "say 素材局;bind "'" "ez42"";
alias "ez42" "say 扣1上车;bind "'" "ez43"";
alias "ez43" "say 暂时不考虑打职业;bind "'" "ez44"";
alias "ez44" "say 打成这样多想想自己原因;bind "'" "ez01"";



alias "nb01" "say NB;bind "'" "nb02"";
alias "nb02" "say 拜师;bind "'" "nb03"";
alias "nb03" "say 收后三名吗;bind "'" "nb04"";
alias "nb04" "say 统一回复：卡了;bind "'" "nb05"";
alias "nb05" "say 666这个入是桂;bind "'" "nb06"";
alias "nb06" "say 我打不过，对面帮忙点个投降;bind "'" "nb07"";
alias "nb07" "say 听不懂，我唐人街的;bind "'" "nb08"";
alias "nb08" "say 我只看到了天赋与努力;bind "'" "nb09"";
alias "nb09" "say 别炸了，人外有人，段上还有段;bind "'" "nb10"";
alias "nb10" "say 我的意识光可鉴人，枪法四面八方。你不能说它一无是处，只能说菜的相得益彰。;bind "'" "nb11"";

alias "nb11" "say 你能打上海major，真是职职又业业啊;bind "'" "nb12"";
alias "nb12" "say 你要是去打职业，damn！king只能走文化课。;bind "'" "nb13"";
alias "nb13" "say 我敢拜师，你敢收吗？;bind "'" "nb14"";
alias "nb14" "say 稍等一下，我装下假肢;bind "'" "nb15"";
alias "nb15" "say 啊？我打残局？;bind "'" "nb16"";
alias "nb16" "say 遗言丁真，鉴定为死活打不过;bind "'" "nb17"";
alias "nb17" "say 如果我游戏玩的是依托构史，那我练枪算不算史上雕花？;bind "'" "nb18"";
alias "nb18" "say 万水千山总是情，放水一把行不行;bind "'" "nb19"";
alias "nb19" "say 我的枪法比较松弛，但我萎缩的意识弥补了这一点;bind "'" "nb20"";
alias "nb20" "say 我的完美战力：1355。按住【F10+Enter】查询完美战力。;bind "'" "nb21"";

alias "nb21" "say 看似还在对枪，其实似了有一会了;bind "'" "nb22"";
alias "nb22" "say 你打的不像透|视，像上层叙事。;bind "'" "nb23"";
alias "nb23" "say 装逼让你;bind "'" "nb24"";
alias "nb24" "say 飞起来！;bind "'" "nb25"";
alias "nb25" "say 不觉得我片叶不沾身的枪法颇具浪漫主义色彩吗？;bind "'" "nb26"";
alias "nb26" "say Ciallo～(∠・ω< )⌒☆;bind "'" "nb27"";
alias "nb27" "say 队友夸我是构史不可或缺的一部分，因为我一人就是大唐盛世。;bind "'" "nb28"";
alias "nb28" "say 鼠标睡着了，不然包赢的。;bind "'" "nb29"";
alias "nb29" "say CS2为我加入了专属地图【唐人街】，赶快来试试吧！;bind "'" "nb30"";
alias "nb30" "say 我患有重度马枪症十八年了，状态好的时候我告诉自己，得上个B，以前被B哥带飞的时候，感觉很帅气。  于是我玩了很多个赛季，每天下班用夜里时间练枪。;bind "'" "nb31"";

alias "nb31" "say 可我实在打不动了，上周刚卸了游戏，如释重负。 刚刚打开手机发现平台还留着，我盘算了一下，玩了十几个赛季，最高的时候就差一把就能上B了。;bind "'" "nb32"";
alias "nb32" "say 每次看你们以菜鸡自嘲，说实话挺羡慕的，因为我真是菜鸡，我不可能笑着说我就菜，我心理承受能力没那么强;bind "'" "nb33"";
alias "nb33" "say 在座各位历史最高段位可能都是A到S，我几个赛季elo加起来也够不着你们的段，赛季结束前我搭子说我能上个B，就roll我一把崭新爪子刀喷漆庆祝，;bind "'" "nb34"";
alias "nb34" "say 事实是最后我连C+的大门也没敲开，赛季结束前最后一把，队友在语音一整局都没说话。每次看你们嘻嘻哈哈说自己是菜鸡，我真的快喘不过气，;bind "'" "nb35"";
alias "nb35" "say 这对你们来说是茶余饭后炸鱼塘的梗，但却是让我无数赛季抬不起头做人的痛，希望朋友们别再炸鱼反串，也给我这种底层人一点生存空间吧，谢谢了。;bind "'" "nb36"";
alias "nb36" "say 文案是编的，人菜是真的。;bind "'" "nb37"";
alias "nb37" "say 年轻人，未来是你们的;bind "'" "nb38"";
alias "nb38" "say 那我马枪没打掉的人头这块谁给我补啊;bind "'" "nb39"";
alias "nb39" "say 大佬，菜菜，带带;bind "'" "nb40"";
alias "nb40" "say 你打赢我并不会收获我的称赞，但故意放水却能收获我的感谢。;bind "'" "nb41"";

alias "nb41" "say 才没有在梦游，只是在CTwalk罢了;bind "'" "nb42"";
alias "nb42" "say 我明明已经用方向盘在玩游戏，为什么还是打不过推着轮椅过去的你;bind "'" "nb43"";
alias "nb43" "say 凭什么就我是马场悟道;bind "'" "nb44"";
alias "nb44" "say 为什么枪枪头？我头上是网易春风精灵吸力这么强？;bind "'" "nb45"";
alias "nb45" "say 队友麦里的无能狂怒我安然入睡，游戏结束后传来的练枪声让我彻夜难眠。;bind "'" "nb46"";
alias "nb46" "say 我可能是你见过的上升空间最大的对手;bind "'" "nb47"";
alias "nb47" "say 这把不知道怎么了，总觉得不知道怎么了。;bind "'" "nb48"";
alias "nb48" "say 你打的不是我，而是还是菜鸡时的自己;bind "'" "nb49"";
alias "nb49" "say 不是哥們，可以摸摸你黃埔軍校的錄取通知書嗎？;bind "'" "nb50"";
alias "nb50" "say 纵死侠骨香，不惭世上英。谁能书阁下，白首太玄经。;bind "'" "nb01"";



alias "ez" "cl_hud_color 7;bind "'" "ez01";bind ralt "nb;""
alias "nb" "cl_hud_color 10;bind "'" "nb01";bind ralt "ez;""
bind "ralt""ez;"
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