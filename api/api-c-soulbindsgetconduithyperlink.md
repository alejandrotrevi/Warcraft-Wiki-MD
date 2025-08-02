# API C Soulbinds.GetConduitHyperlink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Soulbinds|system=Soulbinds}}
Needs summary.
 link = C_Soulbinds.GetConduitHyperlink(conduitID, rank)

==Arguments==
:;conduitID:{{apitype|number}} : {{dbc|soulbindconduit|SoulbindConduit.ID}}
:;rank:{{apitype|number}} : {{dbc|soulbindconduitrank|SoulbindConduitRank.RankIndex}} - Returned from {{api|C_Soulbinds.GetConduitRank}}()

==Returns==
:;link:{{apitype|string}} : [[Hyperlinks#conduit|conduitLink]]

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```