# API C CampaignInfo.GetState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CampaignInfo|system=WarCampaign}}
Needs summary.
 state = C_CampaignInfo.GetState(campaignID)

==Arguments==
:;campaignID:{{apitype|number}}

==Returns==
:;state:{{apitype|Enum.CampaignState}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| align="center" | 0 || Invalid || 
|-
| align="center" | 1 || Complete || 
|-
| align="center" | 2 || InProgress || 
|-
| align="center" | 3 || Stalled || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```