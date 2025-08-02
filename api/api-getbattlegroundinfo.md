# API GetBattlegroundInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a battleground type.
 localizedName, canEnter, isHoliday, isRandom, battleGroundID, mapDescription, bgInstanceID, maxPlayers, gameType, iconTexture, shortDescription, longDescription, hasControllingHoliday = GetBattlegroundInfo(index)

==Arguments==
:;index:{{apitype|number}} - battleground type index, 1 to {{api|GetNumBattlegroundTypes}}().

==Returns==
:;localizedName:{{apitype|string}} - Localized battleground name.
:;canEnter:{{apitype|boolean}} - `true` if the player can queue for this battleground, `false` otherwise.
:;isHoliday:{{apitype|boolean}} - `true` if this battleground is currently granting bonus honor due to a battleground holiday, `false` otherwise.
:;isRandom:{{apitype|boolean}} - `true` if this battleground is the random.
:;battleGroundID:{{apitype|number}} - the ID associated with the Battleground. See `BattlemasterList.db2` for full list.
:;mapDescription:{{apitype|string}} - Localized information about the battleground map.
:;bgInstanceID:{{apitype|number}} - [[InstanceID]] of the battleground map.
:;maxPlayers:{{apitype|number}} - Maximum number of players allowed in the battleground.
:;gameType:{{apitype|string}} - Type of the game (e.g., "CTF" for Capture the Flag). Empty string if none.
:;iconTexture:{{apitype|number}} - Path to the icon texture representing the battleground.
:;shortDescription:{{apitype|string}} - Short description of the battleground.
:;longDescription:{{apitype|string}} - Long description of the battleground.
:;hasControllingHoliday:{{apitype|number}} - `1` if there's a controlling holiday for the battleground, `0` otherwise.

==Patch changes==
* {{Patch 7.2.0|note=Added <code>shortDescription, longDescription</code>.}}
```