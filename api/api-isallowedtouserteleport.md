# API IsAllowedToUserTeleport

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the player can teleport to/from an LFG instance.
 allowedToTeleport = IsAllowedToUserTeleport()

==Returns==
:;allowedToTeleport:{{apitype|boolean}} - true if the player can teleport to/from an LFG instance, false otherwise.

==Details==
* The player cannot teleport out of the solo scenarios introduced in [[Patch 5.2]].

==Patch changes==
* {{Patch 5.2.0|note=Added.}}

==See also==
* {{api|LFGTeleport}}
```