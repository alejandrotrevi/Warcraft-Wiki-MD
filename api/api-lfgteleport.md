# API LFGTeleport

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Teleports the player to or from a LFG dungeon.
 LFGTeleport(toSafety)

==Arguments==
:;toSafety:{{apitype|boolean}} - false to teleport to the dungeon, true to teleport to where you were before you were teleported to the dungeon.

==Example==
 /run LFGTeleport(IsInLFGDungeon())
```