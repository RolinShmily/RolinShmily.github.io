### autoexec.cfg
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
### train.cfg
```ini
//Train
bind "k" "sv_cheats 1;give weapon_knife"
bind "l" "sv_rethrow_last_grenade"
bind "n" "noclip"
bind "p" "sv_cheats 1;bot_kick;mp_buy_anywhere 1;mp_freezetime 0;mp_maxmoney 99999;mp_startmoney 99999;mp_buytime 99999;mp_ignore_round_win_conditions 1; mp_respawn_on_death_ct 1;mp_respawn_on_death_t 1;mp_friendlyfire 1;ammo_grenade_limit_total 6;mp_spectators_max 9; mp_autokick 0; mp_restartgame 1;sv_grenade_trajectory_prac_pipreview 1; sv_grenade_trajectory_prac_trailtime 8;sv_infinite_ammo 2;sv_showimpacts 1;say Practice Enabled"
```
### knife.cfg
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
### lastinv.cfg
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
```
### zeus.cfg
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
### crosshair_view.cfg
```ini
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