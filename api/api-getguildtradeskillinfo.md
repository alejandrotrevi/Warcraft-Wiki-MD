# API GetGuildTradeSkillInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a profession in the guild roster.
 skillID, isCollapsed, iconTexture, headerName, numOnline, numVisible, numPlayers,
 playerName, playerNameWithRealm, class, online, zone, skill, classFileName, isMobile, isAway
     = GetGuildTradeSkillInfo(index)

==Arguments==
:;index:{{apitype|number}} - The index of the tradeskill from GetNumGuildTradeSkill().

==Returns==
:;1. skillID:{{apitype|number}} - The ID for the tradeskill
:;2. isCollapsed:{{apitype|boolean}} - If the tradeskill is a header, whether or not it is expanded in the guild UI
:;3. iconTexture:{{apitype|string}} - The icon for the tradeskill
:;4. headerName:{{apitype|string}} - If the tradeskill is a header, this is the text ("Alchemy", "Jewelcrafting", etc)
:;5. numOnline:{{apitype|number}} - If the tradeskill is a header, this is the number of characters in the guild who have this tradeskill and are online
:;6. numVisible:{{apitype|number}} - If the tradeskill is a header, this is the number of characters in the guild who have this tradeskill and visible (depends on the view offline members checkbox)
:;7. numPlayers:{{apitype|number}} - If the tradeskill is a header, this is the number of characters in the guild who have this tradeskill
:;8. playerName:{{apitype|string}} - If the tradeskill is not a header, this is the name of the character who has this tradeskill
:;9. playerNameWithRealm:{{apitype|string}} - Same as playerName but includes realm, as "name-realm" (with embedded spaces removed)
:;10. class:{{apitype|string}} - If the tradeskill is not a header, this is the (localized?) class of the character who has the tradeskill
:;11. online:{{apitype|boolean}} - If the tradeskill is not a header, this is whether or not the character who has the tradeskill is online
:;12. zone:{{apitype|string}} - If the tradeskill is not a header, this is the zone the character who has the tradeskill is currently in
:;13. skill:{{apitype|number}} - If the tradeskill is not a header, this is the character tradeskill level
:;14. classFileName:{{apitype|string}} - If the tradeskill is not a header, this is the class of the character who has the tradeskill
:;15. isMobile:{{apitype|boolean}} - If the tradeskill is not a header, this is whether or not the character is online with the Armory App
:;16. isAway:{{apitype|number}} - If the tradeskill is not a header, this is whether or not the character is away

==Patch changes==
* {{Patch 5.4.2|note=Added <code>playerNameWithRealm</code> return.}}
```