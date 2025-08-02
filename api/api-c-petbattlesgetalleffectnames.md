# API C PetBattles.GetAllEffectNames

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns all effect parameter names for Pet Battles.
 effect1, effect2, ... = C_PetBattles.GetAllEffectNames()

==Returns==
:;effect1, effect2, ..:{{apitype|string}} - Each return is the name of a different effect parameter for Pet Battles. These effect names can be passed to {{api|C_PetBattles.GetAbilityEffectInfo}} in order to return information about that effect.

==Example==
Returns the damage variance of [[Baby Winston|Baby Winston's]] [[Tesla Cannon]]:
<syntaxhighlight lang="lua">
/dump C_PetBattles.GetAbilityEffectInfo(1625, 1, 1, "variance")
-- 60
</syntaxhighlight>

This function returns an extreme amount of data and is best dealt with by putting the results directly into a table. This is how Blizzard uses it:
<syntaxhighlight lang="lua">
local effectParamStrings = {C_PetBattles.GetAllEffectNames()}
</syntaxhighlight>

==Effects==
The return values as of Patch 11.0.2
<syntaxhighlight lang="lua">
"ability",
"ability 1",
"ability 2",
"accuracy", -- Ability hit chance percentage (e.g. 0%, 25%, 35%, 50%, 85%, 100%, 150%)
"asdf",
"auraabilityid",
"auraid",
"basechancetosucceed",
"bonusdamage",
"bonuspoints",
"bonusstate",
"boost",
"bypasspetpassives",
"casterimmunestate",
"casterstate",
"casterstatevalue",
"chainfailure",
"chance",
"changevalue",
"cooldownmodification",
"dontmiss",
"duration",
"duration2",
"enablereverse",
"evenmorepoints",
"healthpercentage",
"healthpercentthreshold",
"healththreshold",
"increasepertoss",
"index",
"int 1",
"isperiodic",
"lockduration",
"maxallowed",
"maxpoints",
"modifier",
"morepoints",
"newduration",
"none",
"overrideindex",
"percentage",
"points",
"pointsincreaseperuse",
"pointsmax",
"power", -- The base damage or healing of the ability (base power is before being taking level, quality, or breed - effectively a level 1, poor quality pet, with no breed bonuses)
"reportfailsasimmune",
"requiredcasterpettype",
"requiredcasterstate",
"requiredpettype",
"requiredtargetpettype",
"requiredtargetstate",
"sdf",
"slot",
"state",
"statechange",
"statemax",
"statemin",
"statepoints",
"statetomultiplyagainst",
"statetotriggermaxpoints",
"statevalue",
"targetimmunestate",
"targetstate",
"targetstatevalue",
"targetteststate",
"targetteststatevalue",
"threshold",
"tickdownfirstround",
"turnstoadvance",
"unused",
"variance", -- the variance to be applied to power. Base damage or healing will be power±(variance/200)
"weatherstate"
</syntaxhighlight>

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAbilityEffectInfo}}
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]

<!-- luals
---@return string ...
function C_PetBattles.GetAllEffectNames() end
-->
```