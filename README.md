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

Then, at the bottom of the description.ext insert #include "addons\DRNdialogs.hpp"
