```
//tips01
alias "att0" "bind mouse1 +firr1;bind mouse2 +firr2"
alias "att1" "bind mouse1 +attack;bind mouse2 +attack2"

alias "+firr1" "+attack"
alias "-firr1" "-attack;slot2;slot1;att1;"
alias "+firr2" "+attack2"
alias "-firr2" "-attack2;slot2;slot1;att1;"

//Mouse
sensitivity 1.25

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
bind "5" "slot5; att1; switchhandsright"

bind "z" "slot6; switchhandsright" 
bind "x" "slot3; slot7; switchhandsright" 
bind "c" "slot8; switchhandsright" 
bind "6" "slot9; switchhandsright" 
bind "v" "slot10; switchhandsright" 

bind "q" "lastinv; att1;"
bind "i" "+spray_menu"
bind "u" "messagemode2"
bind "y" "messagemode"
bind "alt" "+voicerecord"
bind "mouse4" "clutch_mode_toggle"
bind "mouse5" "player_ping"
bind "mwheeldown" "invnext" 
bind "mwheelup" "invprev"
bind "`" "toggleconsole"

bind "t" "switchhands"
bind "h" "toggleradarscale" 

//cfg
bind "o" "exec autoexec.cfg"
bind "\" "key_listboundkeys"

//Crosshair
cl_crosshair_drawoutline "0"
cl_crosshair_dynamic_maxdist_splitratio "0.3"
cl_crosshair_dynamic_splitalpha_innermod "1"
cl_crosshair_dynamic_splitalpha_outermod "0.5"
cl_crosshair_dynamic_splitdist "7"
cl_crosshair_friendly_warning "0"
cl_crosshair_outlinethickness "0"
cl_crosshair_sniper_show_normal_inaccuracy "0"
cl_crosshair_sniper_width "0"
cl_crosshair_t "0"
cl_crosshairalpha "255"
cl_crosshaircolor 5
cl_crosshaircolor_b "145"
cl_crosshaircolor_g "255"
cl_crosshaircolor_r "0"
cl_crosshairdot "0"
cl_crosshairgap "-4"
cl_crosshairgap_useweaponvalue "0"
cl_crosshairsize "1"
cl_crosshairstyle "4"
cl_crosshairthickness "1"
cl_crosshairusealpha "1"

//Gun's view
viewmodel_fov 64
viewmodel_offset_x 2
viewmodel_offset_y 1.5
viewmodel_offset_z -1.5
viewmodel_presetpos 3

//Radar
cl_radar_always_centered "0"
cl_radar_scale "0.37"
cl_hud_radar_scale "1"
cl_teammate_colors_show 2

//Others
cl_hud_color "11"
con_enable "1"
fps_max 999
cl_join_advertise "2"
cl_use_opens_buy_menu "0" 
cl_dm_buyrandomweapons 0 
gameinstructor_enable "0"
cl_autohelp "false"
mm_dedicated_search_maxping "70"
func_break_max_pieces 0
r_drawtracers_firstperson 0
r_fullscreen_gamma 2.4
cl_teamid_overhead_mode 3
cl_use_opens_buy_menu true

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

//nob
alias "noob01" "say ⣿⣿⣿⣿⣿⠀⣿⣿⣿⣿;bind "[" "noob02"";
alias "noob02" "say ⣿⣿⣿⣿⣿⠀⣿⣿⣿⣿;bind "[" "noob03"";
alias "noob03" "say ⣿⣿⣿⡿⢿⠀⡿⢿⣿⣿;bind "[" "noob04"";
alias "noob04" "say ⣿⡏⢹⠀⢸⠀⡇⠀⣿⣿;bind "[" "noob05"";
alias "noob05" "say ⣿⡇⠈⠀⠈⠀⠀⠀⡏⢻;bind "[" "noob06"";
alias "noob06" "say ⣿⡇⠀⠀⠀⠀⠀⠀⠁⣼;bind "[" "noob07"";
alias "noob07" "say ⣿⣇⠀⠀⠀⠀⠀⠀⣰⣿;bind "[" "noob08"";
alias "noob08" "say ⣿⣧⣤⣤⣤⣤⣤⣤⣿⣿;bind "[" "noob01""
bind "[" "noob01"

//good
alias "good01" "say ⣿⣿⣿⣿⣿⣿⣿⡏⠀⠈⢿⣿⣿⣿⣿⣿;bind "]" "good02"";
alias "good02" "say ⣿⣿⣿⣿⣿⣿⣿⡇⠀⠀⢸⣿⣿⣿⣿⣿;bind "]" "good03"";
alias "good03" "say ⣿⠿⠿⠿⢿⡿⠟⠀⠀⠀⠸⠿⠿⣿⣿⣿;bind "]" "good04"";
alias "good04" "say ⣿⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⢀⣿;bind "]" "good05"";
alias "good05" "say ⣿⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⢀⣿;bind "]" "good06"";
alias "good06" "say ⣿⠀⠀⠀⠀⡇⠀⠀⠀⠀⠀⠀⠀⠀⢀⣿;bind "]" "good07"";
alias "good07" "say ⣿⠀⠀⠀⢀⡇⠀⠀⠀⠀⠀⠀⠀⠀⢈⣿;bind "]" "good08"";
alias "good08" "say ⣿⣷⣶⣶⣿⣿⣷⣶⣶⣶⣶⣶⣿⣾⣿⣿;bind "]" "good01"";
bind "]" "good01"

//Ending
echo AutoConfig Enabled!
say Hello!

//Train
bind "k" "give weapon_knife"
bind "l" "sv_rethrow_last_grenade"
bind "n" "noclip"
bind "p" "sv_cheats 1;bot_kick;mp_buy_anywhere 1;mp_freezetime 0;mp_maxmoney 99999;mp_startmoney 99999;mp_buytime 99999;mp_ignore_round_win_conditions 1; mp_respawn_on_death_ct 1;mp_respawn_on_death_t 1;mp_friendlyfire 1;ammo_grenade_limit_total 6;mp_spectators_max 9; mp_autokick 0; mp_restartgame 1;sv_grenade_trajectory_prac_pipreview 1; sv_grenade_trajectory_prac_trailtime 8;sv_infinite_ammo 2;sv_showimpacts 1;say Practice Enabled"
```