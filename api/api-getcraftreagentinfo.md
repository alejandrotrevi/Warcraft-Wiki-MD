# API GetCraftReagentInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
This command tells the caller which the name of the reagent, path to the used texture, number of required reagents, and number of said reagents that the caller currently has in their bags. 
 name, texturePath, numRequired, numHave = GetCraftReagentInfo(index, n)

==Parameters==
===Arguments===
:;index:{{apitype|number}} - starting at 1 going down to X number of possible crafts, where 1 is the top-most listed craft.
:;n:{{apitype|number}} - starting at 1 to X, where X is the total number of reagents said craft requires.

===Returns===
:;name:Name of the reagent required. ie, "Large Brilliant Shard"
:;texturePath:Path to the required item texture. ie, "Interface\Icons\INV_Enchant_ShardBrilliantLarge"
:;numRequired:Numeric. Number of total required reagents.
:;numHave:Numeric. Number of total required reagents that the user has on them currently.

==Patch changes==
* {{Patch 3.0.2|note=Removed.}}
```