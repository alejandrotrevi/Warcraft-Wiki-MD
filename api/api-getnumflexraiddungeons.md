# API GetNumFlexRaidDungeons

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of available [[Flexible Raid]] instances.
 numInstances = GetNumFlexRaidDungeons()

==Returns==
:;numInstances:{{apitype|number}} - number of instances available for flexible raid groups.

==Details==
* The return value does not take your character or instance availability into account; it is simply the number of flexible raid instances the client is aware of.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|GetFlexRaidDungeonInfo}}
```