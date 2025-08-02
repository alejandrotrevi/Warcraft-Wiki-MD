# API GetCraftDescription

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
This command returns a string description of what the current craft does.  

 craftDescription = GetCraftDescription(index)

==Parameters==
===Arguments===
:;index:{{apitype|number}} - Number from 1 to X number of total crafts, where 1 is the top-most craft listed.

===Returns===
:;craftDescription:{{apitype|string}} - Returns, for example, "Permanently enchant a two handed melee weapon to grant +25 Agility."

==Patch changes==
* {{Patch 3.0.2|note=Removed.}}
```