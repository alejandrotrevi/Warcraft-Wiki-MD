# API C PlayerInfo.GUIDIsPlayer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the GUID belongs to a player.
 isPlayer = C_PlayerInfo.GUIDIsPlayer(guid)

==Arguments==
:;guid:{{apitype|string}} - The GUID to be checked.

==Returns==
:;isPlayer:{{apitype|boolean}} - True if the GUID represents a player unit, or false if not.

==Details==
* This function currently as of patch 9.0.2 only validates that the supplied GUID begins with the string <code>"Player-"</code>.

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```