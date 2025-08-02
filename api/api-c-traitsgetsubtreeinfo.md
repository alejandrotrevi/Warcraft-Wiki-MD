# API C Traits.GetSubTreeInfo

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Needs summary.
 subTreeInfo = C_Traits.GetSubTreeInfo(configID, subTreeID)

==Arguments==
:;configID:{{apitype|number}}
:;subTreeID:{{apitype|number}}

==Returns==
:;subTreeInfo:{{apitype|TraitSubTreeInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|ID}} || {{apitype|number}} || 
|-
| {{apiname|name}} || {{apitype|string?}} || 
|-
| {{apiname|description}} || {{apitype|string?}} || 
|-
| {{apiname|iconElementID}} || {{apitype|textureAtlas?}} || 
|-
| {{apiname|traitCurrencyID}} || {{apitype|number?}} || 
|-
| {{apiname|isActive}} || {{apitype|boolean}} || 
|-
| {{apiname|subTreeSelectionNodeIDs}} || {{apitype|number[]}} || SubTreeSelectionNodes whose choice entries include this SubTree
|-
| {{apiname|posX}} || {{apitype|number}} || Center X node position calculated from the posX values of all of this subTree's nodes
|-
| {{apiname|posY}} || {{apitype|number}} || Topmost Y node position taken from the posY values of all of this subTree's nodes
|}

{{apinavbox|C_Traits}}
```