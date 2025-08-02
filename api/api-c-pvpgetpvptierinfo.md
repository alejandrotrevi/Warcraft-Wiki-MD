# API C PvP.GetPvpTierInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 pvpTierInfo = C_PvP.GetPvpTierInfo(tierID)

==Arguments==
:;tierID:{{apitype|number}}

==Returns==
:;pvpTierInfo:structure - PvpTierInfo (nilable)
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| descendRating || {{apitype|number}} || 
|-
| ascendRating || {{apitype|number}} || 
|-
| descendTier || {{apitype|number}} || 
|-
| ascendTier || {{apitype|number}} || 
|-
| pvpTierEnum || {{apitype|number}} || 
|-
| tierIconID || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```