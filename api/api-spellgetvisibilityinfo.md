# API SpellGetVisibilityInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__

Checks if the spell should be visible, depending on spellId and raid combat status
 hasCustom, alwaysShowMine, showForMySpec = SpellGetVisibilityInfo(spellId, visType)

==Arguments==
:;spellId:{{apitype|number}} - The ID of the spell to check
:;visType:{{apitype|string}} - either "RAID_INCOMBAT" if in combat, "RAID_OUTOFCOMBAT" otherwise

==Returns==
:;hasCustom:{{apitype|boolean}} - whether the spell visibility should be customized, if false it means always display
:;alwaysShowMine:{{apitype|boolean}} - whether to show the spell if cast by the player/player's pet/vehicle (e.g. the Paladin Forbearance debuff)
:;showForMySpec:{{apitype|boolean}} - whether to show the spell for the current specialization of the player

==Details==
* This is used by Blizzard's compact frame until 8.2.5, for whether it should be shown in the raid UI.<ref>{{ref FrameXML|Blizzard_Deprecated/Deprecated_8_2_5.lua|8.2.5|31960|159|20200428}}</ref>

==Exernal links==
{{Elinks-api}}

==References==
{{Reflist|2}}
```