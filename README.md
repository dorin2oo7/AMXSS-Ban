# AMXSS-Ban
The most advances snapshop + ban plugin for Counter Strike

.:: Description ::.

THE MOST ADVANCED SNAPSHOT+BAN PLUGIN!


IMPORTANT !!! For the ban menu you have to type the reason before ban occurs ! If you do not apply a reason before ban occurs the NO_REASON_MENU multilingual line will 'say' No Reason Submission as reason !

Thank's everyone for their help/support on developing this plugin !

    Make snapshots of a player by amx_ss command (saved on targets PC).
    Ban players by AmxModX Ban or AmxBans (v5.x or v6.x) and also takes snapshots by amx_ssban command.
    Menu banning and snapshot taking by amx_ssbanmenu command.
    Inside snapshots are displayed messages with players details like IP, SteamID, Name, Country, Unban site etc.
    The printed details could be in HUD (center top), Chat or both.
    Check Admin Commands to see how does the commands works.
    Check Available CVAR's to see what you can change within this plugin.
    See snapshots below to see how it works.
    Check F.A.Q. first if you have trouble in using this plugin.



.:: ToDo ::.

- Add Ban Menu - added on 26.07.2009 - by Fysiks
- Add reason for ban menu - added on 31.07.2009 - by Fysiks
- Add support for AmxBans v6.x - added on 09.07.2010 - by Fysiks
- Add AMX SSBan into amxmodxmenu - added on 30.01.2011 - by Fysiks



.:: F.A.Q. ::.

*NEW*
Q: How to add Amx SSBan into amxmodxmenu?
A: Use the plugin (menufront.sma) modified by fysiks from HERE (or attached bellow).
*NEW*

Q: Where are the snapshots saved?
A: The snapshots are saved on targets computer in cstrike folder.

Q: Why does the plugin not loading with server?
A: You may need to check installation again to make sure that amx_ssban.amxx exist in plugins folder, and the line amx_ssban.amxx exist on a new line in plugins.ini.

Q: Why does the plugin appears in server console unknown when I type amxx plugins ?
A: You have to make sure that the plugin named amx_ssban.amxx exists in plugins folder and the line amx_ssban.amxx exists in plugins.ini.

Q: The menu is not working. Why ?
A: Make sure you installed the last version (above 2.0) !

Q: Why does the ban not working ?
A: You need to use above v2.4 because of new steam updates that are not allowing to many commands in one line.


.:: Installing ::.

    Upload amx_ssban.amxx into mod_dir/addons/amxmodx/plugins (mod_dir = cstrike, czero, dod etc)
    Upload menufront.amxx into mod_dir/addons/amxmodx/plugins (mod_dir = cstrike, czero, dod etc) ONLY if you want amx ssban in amxmodxmenu
    Upload screen_message.txt into mod_dir/addons/amxmodx/data/lang
    Open plugins.ini from mod_dir/addons/amxmodx/configs
    Add after '; Custom - Add 3rd party plugins here' on a new line like follows:
    Code:

    amx_ssban.amxx

    Save and close plugins.ini
    Restart Server (recommended) or Change Map


If you use AMXBANS you need to follow this steps:

    Open amxx_ssban.sma and find line 113 that looks like this:
    PHP Code:
    #define AMXBANS 0 // Set this to 1 to enable AmxBans support. (Uses amx_ban <minutes> <userid> [reason]) 
    Change 0 into 1
    Save and Close
    Recompile plugin
    Move compiled *.amxx from compile folder to plugins folder and replace the old one.



.:: Available CVAR's ::.

    amx_ssdelay "1.0"
        Delay between snapshots (Def.: "1.0") WARNING has to be .0 as is float
    amx_bandelay "10.0"
        Delay before ban is done (Def.: "10.0") WARNING has to be .0 as is float
    amx_ssnumber "3"
        Number of snapshots to take (Def.: "3")
    amx_website ""
        Unban request site (Def.: "www.yoursite.com")
    amx_msg_type "3"
        Info player/admin messages 1 - chat | 2- hud | 3- chat+hud (Def.: "3")



.:: Admin Commands ::.

    amx_ss <name or #userid>
        Make Snapshots on target !
    amx_ssban <name or #userid> <minutes> [reason]
        if #define AMXBANS 0 bans will be done by AMXMODX (Default) and usage will be above one !
    amx_ssban <minutes> <name or #userid> [reason]
        if #define AMXBANS 1 bans will by done by AMXBANS and the usage will be above one !
    amx_ssmenu
        Pop up the snapshot menu - made by Fysiks
    amx_ssbanmenu
        Pop up the ban menu - made by Fysiks


.:: Notes ::.

You can change/modify chat message colors in the language *.txt file located in addons/amxmodx/data/lang named screen_message.txt !
Message colors usage:
- !y - Yellow (Normal chat color)
- !t - Team Color (Red=T, Blue=CT, Grey=Spec)
- !g - Green


.:: Screenshots ::. (N/A anymore)

AMX SSBan Menu with chat and HUD messages.

Ban menu appear only for admins !
HUD and/or Chat messages appear only for target player.

?

Ban reason message waiting:

?

.:: Translations ::.

Code:

[en] English - Teascu Dorin
[ro] Romanian - Teascu Dorin
[es] Spanish - AfteR.
[de] German - master4life & KadiR
[bg] Bulgarian - InquiSitoR-bG
[pl] Polish - merkava
[sv] Swedish - D-TOX & zacky
[nl] Dutch - crazyeffect
[pr] Puerto Rico - One
[lt] Lithuanian - hleV
[bp] Brazilian Portuguese - Bummps
[fr] French - arkshine
[sr] Serbian - rsbane
[lv] Latvian - NiHiLaNTh
[sk] Slovakian - Seehank
[da] Danish - Jelle
[ru] Russian - CKOTuHA
[tc] Traditional Chinese - biscuit628
[cn] Simplified Chinese - biscuit628
[ar] Arabic - Dr.eNd
[vi] Vietnamese - decongamco
[fi] Finnish - jonnzus
[et] Estonian - trollz0r
[tr] Turkish -Secondry.

Any new translations are useful !!!


.:: Thanks & Credits ::.

    Fysiks - added ban menu and optimized the plugin. Added AmxBans v6.x support, and much more.
    Alka - stock color print
    hackandmore - used his plugin to learn how to use amx_msg_type cvar
    AMXX Dev Team for using their amxmodx ban script
    uTg | bigpapajiggs for using part of his plugin Admin Screen2 script about delay between snapshots
    Any other plugins authors that made this type of plugin and this community for all the support provided !



.:: Change Log ::.

Code:

10.Jul.2010 - v2.6 - [ADDED] support for AmxBans v6.x (by Fysiks)
    [FIXED] lang file by saving it as Unicode without BOM
20.Aug.2009 - v2.5 - [ADDED] HUD flashing message to ask reason submission from admin
17.Aug.2009 - v2.4 - [FIXED] Amx Mod X banning issue
31.Jul.2009 - v2.3 - [ADDED] reason submission for menu bans
26.Jul.2009 - v2.2 - [ADDED] menu for taking snapshots - by Fysiks
    [CHANGED] the plugin name from AMXX SSBan w/ Menu in simple AMX SSBan
24.Jul.2009 - v2.1 - [REMOVED] amx_ban_type cvar
    [CHANGED] the script for easy usage of bantype (optimized by Fysiks)
23.Jul.2009 - v2.0 - [ADDED] ban menu - Al the work provided by Fysiks
11.May.2009 - v1.9.5 - [ADDED] tasks controlled by cvar for bans
    [ADDED] cvar amx_bandelay - Delay before ban is done (Def.: 10.0)
07.May.2009 - v1.9.1 - [FIXED] the usage of command on immunity admins.
        You can take snapshots of admins with immunity
06.May.2009 - v1.9 - [ADDED] to AMXX Snapshot a task to take the snapshots with time delay
    [ADDED] cvar amx_ssdelay - Delay between snapshots (Def.: 1)
    [ADDED] cvar amx_ssnumber - Number of snapshots to take (Def.: 3)
    [ADDED] possibility of taking snapshots on immunity admins
06.May.2009 - v1.8.1 beta - [REMOVED] NO ACCESS console message as Fysiks said that
        'if(!cmd_access...' already does this
06.May.2009 - v1.8 beta - [CLEANED] up the plugin (some script arranging)
    [REMOVED] amx_chattag - it was irelevant... left [AMXX] by default as tag
    [ADDED] bans by AMXMODX - THX AMXX Dev Team for ban code
    [ADDED] cvar amx_ban_type - 0- Disabled | 1- AmxModX Ban | 2- AmaBans Ban
    [ADDED] possibility of taking snapshots and banning admins with immunity
        (not working for AMXBANS as is used by server_cmd)
    [ADDED] the console print to inform a player/admin about no acces for command
03.May.2009 - v1.7 beta - [ADDED] command amx_ssban to use bans by AMXBANS
28.Apr.2009 - v1.6 - [CHANGED] from 'if(get_pcvar_num...' to switch Message type with case
18.Apr.2009 - v1.5 - [ADDED] cvar amx_msg_type - 1 - chat | 2- hud | 3- chat+hud (Def: "1")
    [ADDED] hud message for player data (controled by cvar)
    [ADDED] Polish translation
17.Apr.2009 - v1.4 - [ADDED] to cache SteamID also in the snapshots - THX xPaw
17.Apr.2009 - v1.3 - [CHANGED] cvar to pcvar - THX xPaw for pointing that out !
17.Apr.2009 - v1.2 - [ADDED] cvar amx_chattag - Make any tag you like in chat
16.Apr.2009 - v1.1 - [ADDED] Multilingual
15.Apr.2009 - v1.0 - Initial release


.:: Game Monitor ::.

Server that using This Plugin


.:: Downloads ::.
- OLD Versions in *.zip file !
- menufront.amxx is only for who wants to add amx ssban into amxmodxmenu
