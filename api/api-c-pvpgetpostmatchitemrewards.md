# API C PvP.GetPostMatchItemRewards

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 rewards = C_PvP.GetPostMatchItemRewards()

==Returns==
:;rewards:{{apitype|PVPPostMatchItemReward[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| type || {{apitype|string}} || 
|-
| link || {{apitype|string}} || 
|-
| quantity || {{apitype|number}} || 
|-
| specID || {{apitype|number}} || 
|-
| sex || {{apitype|number}} || 
|-
| isUpgraded || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 8.2.0|note=Added.}}
```