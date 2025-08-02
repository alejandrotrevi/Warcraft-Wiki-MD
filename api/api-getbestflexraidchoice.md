# API GetBestFlexRaidChoice

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the dungeon ID of the most appropriate Flex Raid instance for the player.
 flexDungeonID = GetBestFlexRaidChoice()

==Returns==
:;flexDungeonID:{{apitype|number}} - dungeon ID of the most appropriate Flex Raid instance for the player, or nil if no Flex Raids are currently appropriate.

==Details==
* If there are no flex raids available for your character (i.e. you're below level 90), this function returns nil.
* Otherwise, it returns the dungeon ID of the most advanced Flex Raid the player is eligible for.
* You can retrieve information about the suggested flex raid using {{api|GetLFGDungeonInfo}}.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}
```