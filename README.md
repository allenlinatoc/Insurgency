# Insurgency
These are sourcemod plugins for insurgency.<br>

Don't forget to checkout my server.<br>
Website: http://insurgency.pro/

You can check your server info too by putting your server IP and port (port is optional. Default is 27015).<br>
Example: http://insurgency.pro/server/108.61.136.218

Also mostly these plugins are for Coop Server.

 * <a href='#cmap-102'>CMap (1.0.2)</a>
 * <a href='#botcount-101'>Botcount (1.0.1) (No longer need)</a>
 * <a href='#limit-smoke-102'>Limit Smoke (1.0.2)</a>
 * <a href='#bot-flashbang-101'>Bot Flashbang (1.0.1)</a>
 * <a href='#spawn-protection-100'>Spawn Protection (1.0.0)</a>
 * <a href='#teammate-damage-100'>Teammate Damage (1.0.0)</a>
 * <a href='#vote-kick-immunity-100'>Vote Kick Immunity (1.0.0)</a>
 * <a href='#no-resupply-100'>No Resupply (1.0.0)</a>
 * <a href='#bot-aim-100'>Bot Aim (1.0.0)</a><br><br>
 


### CMap (1.0.2)
CMap is use to change map. It a really simple plugin. I made this because someone saying the sm_map off from sourcemod not working in insurgency.<br>
Admins with flag b will able to use this command.<br>

#### Plugin
[plugins/CMap.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/CMap.smx?raw=true)

#### Source
[scripting/CMap.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/CMap.sp)

#### Command List
```
cmap <map name> <gamemode>
changemap <map name> <gamemode>
```

#### Example
```
cmap sinjar_coop checkpoint
changemap sinjar_coop checkpoint

cmap sinjar hunt
```


### Botcount (1.0.1) (No longer need)
Botcount plugin is use to fix the coop bot count issue that not scaling with the amount of players in the latest patch.<br>
There is no config file for this.<br>
All you have to do is download and put it in your plugins folder and have it load then it finish.<br>
Would be better if you set `mp_coop_lobbysize` in your `server.cfg` to let this plugin know how many players is going to be in your server. This is just optional.<br>
(This is a reharsh version from jared ballou coop lobby overwrite)<br><br>

**Note:** When you first load your server, the plugin might not work. You will have to change map or reload the map one time to have it start working.<br><br>

**NO LONGER NEED:** NWI had fix the bot issue so this plugin no longer need.<br>

#### Plugin
[plugins/botcount.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/botcount.smx?raw=true)

#### Source
[scripting/botcount.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/botcount.sp)


### Limit Smoke (1.0.2)
This is use to limit the amount of smoke player can carry. I made this one when I run vanilla server. It really useful for server that running COOP and not using custom theater.<br>
The reason I made this is to prevent player from abusing the smoke grenades making bots just standing still.<br>
Config file for this plugin will also auto create on run. It will locate in your cfg/sourcemod folder.<br>

#### Plugin
[plugins/limit_smoke.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/limit_smoke.smx?raw=true)

#### Source
[scripting/limit_smoke.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/limit_smoke.sp)

#### Command List
```
sm_ins_limit_smoke_enabled 1 (sets whether limit smoke are enabled)
sm_ins_limit_smoke_amount 1 (amount of smoke that player can bring at a time)
```


### Bot Flashbang (1.0.1)
This also for coop vanilla server that don't use custom theater file.<br>

What exactly this do?<br>
Basically it replace the bot smoke grenade into a flashbang grenade.<br>
If bot keep throwing smokes, players will just camp in the smoke. Bot won't able to see players but players able to see bot in smoke.<br>
Instead of throwing smokes giving player handicap, you make them throw flashbang.<br>

#### Plugin
[plugins/bot_flashbang.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/bot_flashbang.smx?raw=true)

#### Source
[scripting/bot_flashbang.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/bot_flashbang.sp)


### Spawn Protection (1.0.0)
This spawn protection plugin will prevent player from taking any damage right away after they spawn. Obviously, you know what exactly it do.<br>
Usually before the round start, there is a timer count down. But you also spawn before the round start. So the spawn protection will start count down. However, this plugin will add that count down timer to the spawn protection timer to prevent your spawn protection timer from running out before the round start.<br>

This also work for Coop. You don't have to worry about the bot going to have spawn protection because they won't!

#### Plugin
[plugins/SpawnProtection.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/SpawnProtection.smx?raw=true)

#### Source
[scripting/SpawnProtection.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/SpawnProtection.sp)


### Teammate Damage (1.0.0)
This plugin is to control the teammate damage. I made this one to prevent my bots from teamkilling each other. You can also use this in PvP Server but it will be pretty useless tho.<br>
There is a config file for this. Just install it and change anything in the config file to your liking.

#### Plugin
[plugins/teammate_damage.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/teammate_damage.smx?raw=true)

#### Source
[scripting/teammate_damage.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/teammate_damage.sp)


### Vote Kick Immunity (1.0.0)
This plugin is to prevent player from vote kick admins using the original vote from the game. The plugin will use immunity base on sourcemod admin config (It also work with admin group config obviously). Admin with lower immunity than the other admin, will not able to vote them. If user not admin, they will only able to vote kick other user that isn't admin.

#### Plugin
[plugins/ins_kickvote_immunity.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/ins_kickvote_immunity.smx?raw=true)

#### Source
[scripting/ins_kickvote_immunity.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/ins_kickvote_immunity.sp)


### No Resupply (1.0.0)
Don't want play to resupply? This is just a simple plugin block the cvar resupply command to prevent player to resupply. It really useful for PvP server that don't want player to resupply their gears.

#### Plugin
[plugins/no_resupply.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/no_resupply.smx?raw=true)

#### Source
[scripting/no_resupply.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/no_resupply.sp)



### Bot Aim (1.0.0)
What exactly is bot aim? Bot aim is a plugin that give bot full aimbot on players. They will target the closest player and will try to headshot player with every single bullet. Its really deadly. This work really well on coop server with the highest bot difficulty.

#### Plugin
[plugins/ins_botaim.smx](https://github.com/zWolfi/Insurgency/blob/master/plugins/ins_botaim.smx?raw=true)

#### Source
[scripting/ins_botaim.sp](https://github.com/zWolfi/Insurgency/blob/master/scripting/ins_botaim.sp)
