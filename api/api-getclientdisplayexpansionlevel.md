# API GetClientDisplayExpansionLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Expansion}}
Returns the expansion level of the game client.
 expansionLevel = GetClientDisplayExpansionLevel()

==Returns==
:;expansionLevel:{{apitype|number}}
{{:LE_EXPANSION}}

==Example==
Before and after updating to the 9.0.1 pre-patch.
 /dump GetClientDisplayExpansionLevel() -- 7 -> 8

==Patch changes==
* {{Patch 7.3.2|note=Added.}}
```