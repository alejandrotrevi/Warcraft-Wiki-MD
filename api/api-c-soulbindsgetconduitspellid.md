# API C Soulbinds.GetConduitSpellID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Soulbinds|system=Soulbinds}}
Needs summary.
 spellID = C_Soulbinds.GetConduitSpellID(conduitID, conduitRank)

==Arguments==
:;conduitID:{{apitype|number}} : {{dbc|soulbindconduit|SoulbindConduit.ID}}
:;conduitRank:{{apitype|number}} : {{dbc|soulbindconduitrank|SoulbindConduitRank.RankIndex}} - Returned from {{api|C_Soulbinds.GetConduitRank}}()

==Returns==
:;spellID:{{apitype|number}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```