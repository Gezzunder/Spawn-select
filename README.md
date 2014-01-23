Spawn-select
============

Graphic spawn select for Dayz Taviana.  Works only for taviana.

Place the files within your addons folder.

at the bottom of your init.sqf (after "#include "\z\addons\dayz_code\system\BIS_Effects\init.sqf") place;

waitUntil {!isNil ("PVDZE_plr_LoginRecord")};
if (dayzPlayerLogin2 select 2) then
{
    [] execVM "addons\DRNSpawn.sqf";
};

Next, at the bottom of your description.ext insert #include "addons\DRNdialogs.hpp"

The next step is within your server.pbo

Locate, within the compiles folder, and look for dayzPlayerLogin2 = [_worldspace,_state]; (it's about line 236)

Change that to dayzPlayerLogin2 = [_worldspace,_state,_randomSpot];

Repack your PBOs (don't forget the path property for the server.pbo) and you're done.
