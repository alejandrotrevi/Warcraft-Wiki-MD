# API C CampaignInfo.GetFailureReason

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CampaignInfo|system=WarCampaign}}
Needs summary.
 failureReason = C_CampaignInfo.GetFailureReason(campaignID)

==Arguments==
:;campaignID:{{apitype|number}}

==Returns==
:;failureReason:{{apitype|CampaignFailureReason?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| text || {{apitype|string}} || 
|-
| questID || {{apitype|number?}} || 
|-
| mapID || {{apitype|number?}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```