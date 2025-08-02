# API C LFGList.GetLfgCategoryInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGList|system=LFGList}}
Needs summary.
 categoryData = C_LFGList.GetLfgCategoryInfo(categoryID)

==Arguments==
:;categoryID:{{apitype|number}}

==Returns==
:;categoryData:{{apitype|LfgCategoryData}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| searchPromptOverride || {{apitype|string?}} || 
|-
| separateRecommended || {{apitype|boolean}} || 
|-
| autoChooseActivity || {{apitype|boolean}} || 
|-
| preferCurrentArea || {{apitype|boolean}} || 
|-
| showPlaystyleDropdown || {{apitype|boolean}} || 
|-
| allowCrossFaction || {{apitype|boolean}} || <font color="green">9.2.5</font>
|}

==Patch changes==
* {{Patch 9.1.5|note=Added.}}
```