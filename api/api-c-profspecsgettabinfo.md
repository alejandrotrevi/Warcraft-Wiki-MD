# API C ProfSpecs.GetTabInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ProfSpecs|system=ProfessionSpecUI}}
Needs summary.
 tabInfo = C_ProfSpecs.GetTabInfo(tabTreeID)

==Arguments==
:;tabTreeID:{{apitype|number}}

==Returns==
:;tabInfo:{{apitype|ProfTabInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| rootNodeID || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| rootIconID || {{apitype|number}} || <font color="green">10.0.7</font>
|-
| highlights || {{apitype|ProfTabHighlight[]}} || <font color="green">10.0.7</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ ProfTabHighlight
! Field !! Type !! Description
|-
| description || {{apitype|string}} || 
|}
```