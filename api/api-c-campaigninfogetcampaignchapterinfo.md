# API C CampaignInfo.GetCampaignChapterInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CampaignInfo|system=WarCampaign}}
Needs summary.
 campaignChapterInfo = C_CampaignInfo.GetCampaignChapterInfo(campaignChapterID)

==Arguments==
:;campaignChapterID:{{apitype|number}}

==Returns==
:;campaignChapterInfo:{{apitype|CampaignChapterInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| rewardQuestID || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```