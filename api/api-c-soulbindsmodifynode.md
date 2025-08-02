# API C Soulbinds.ModifyNode

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Soulbinds|system=Soulbinds}}
Needs summary.
 C_Soulbinds.ModifyNode(nodeID, conduitID, type)

==Arguments==
:;nodeID:{{apitype|number}}
:;conduitID:{{apitype|number}} : {{dbc|soulbindconduit|SoulbindConduit.ID}}
:;type:{{apitype|Enum.SoulbindConduitTransactionType}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| align="center" | 0 || Install || 
|-
| align="center" | 1 || Uninstall || 
|}

==Patch changes==
* {{Patch 9.0.2|note=Added.}}
```