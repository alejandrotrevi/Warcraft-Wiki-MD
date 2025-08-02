# API C MajorFactions.GetRenownRewardsForLevel

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MajorFactions|system=MajorFactionsUI}}
Needs summary.
 rewards = C_MajorFactions.GetRenownRewardsForLevel(majorFactionID, renownLevel)

==Arguments==
:;majorFactionID:{{apitype|number}}
:;renownLevel:{{apitype|number}}

==Returns==
:;rewards:{{apitype|MajorFactionRenownRewardInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|renownRewardID}} || {{apitype|number}} || 
|-
| {{apiname|uiOrder}} || {{apitype|number}} || 
|-
| {{apiname|isAccountUnlock}} || {{apitype|boolean}} || <font color="green">11.0.0</font>
|-
| {{apiname|itemID}} || {{apitype|number?}} || 
|-
| {{apiname|spellID}} || {{apitype|number?}} || 
|-
| {{apiname|mountID}} || {{apitype|number?}} || 
|-
| {{apiname|transmogID}} || {{apitype|number?}} || 
|-
| {{apiname|transmogSetID}} || {{apitype|number?}} || 
|-
| {{apiname|titleMaskID}} || {{apitype|number?}} || 
|-
| {{apiname|transmogIllusionSourceID}} || {{apitype|number?}} || 
|-
| {{apiname|icon}} || {{apitype|fileID?}} || 
|-
| {{apiname|name}} || {{apitype|string?}} || 
|-
| {{apiname|description}} || {{apitype|string?}} || 
|-
| {{apiname|toastDescription}} || {{apitype|string?}} || 
|}
```