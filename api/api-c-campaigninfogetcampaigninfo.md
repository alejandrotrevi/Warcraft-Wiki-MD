# API C CampaignInfo.GetCampaignInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CampaignInfo|system=WarCampaign}}
Needs summary.
 campaignInfo = C_CampaignInfo.GetCampaignInfo(campaignID)

==Arguments==
:;campaignID:{{apitype|number}}

==Returns==
:;campaignInfo:{{apitype|CampaignInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|description}} || {{apitype|string}} || 
|-
| {{apiname|uiTextureKit}} || {{apitype|textureKit}} || <font color="green">9.0.1</font>
|-
| {{apiname|isWarCampaign}} || {{apitype|boolean}} || <font color="green">9.0.1</font>
|-
| {{apiname|usesNormalQuestIcons}} || {{apitype|boolean}} || <font color="green">10.1.7</font>
|-
| {{apiname|isContainerCampaign}} || {{apitype|boolean}} || <font color="green">10.1.7</font>
|-
| {{apiname|sortAsNormalQuest}} || {{apitype|boolean}} || <font color="green">11.0.2</font>
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```