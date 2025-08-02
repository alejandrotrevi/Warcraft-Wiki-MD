# API UnitIsCivilian

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Determine whether a unit is a civilian (low level enemy faction NPC that counts as a dishonorable kill).
 isCivilian = UnitIsCivilian(unit)

==Arguments==
:;[[unit]]:{{apitype|string}} - Only works on enemy faction NPCs.

==Returns==
:;isCivilian:{{apitype|boolean}}

==Patch changes==
* {{Patch 2.3.0|note=Removed. Dishonorable kills were removed from the Honor system.}}
* {{Patch 1.6.0|note=Added.}}
```