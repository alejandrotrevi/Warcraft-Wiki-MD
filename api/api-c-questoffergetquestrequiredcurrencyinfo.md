# API C QuestOffer.GetQuestRequiredCurrencyInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestOffer|system=QuestOffer}}
Needs summary.
 questRequiredCurrencyInfo = C_QuestOffer.GetQuestRequiredCurrencyInfo(questRewardIndex)

==Arguments==
:;questRewardIndex:{{apitype|number}}

==Returns==
:;questRequiredCurrencyInfo:{{apitype|QuestRequiredCurrencyInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|texture}} || {{apitype|fileID}} || 
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|currencyID}} || {{apitype|number}} || 
|-
| {{apiname|quality}} || {{apitype|number}} || 
|-
| {{apiname|requiredAmount}} || {{apitype|number}} || 
|}
```