# API C Traits.GetEntryInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Retrieves Node Entry information.
 entryInfo = C_Traits.GetEntryInfo(configID, entryID)

==Arguments==
:;configID:{{apitype|number}}
:;entryID:{{apitype|number}}

==Returns==
:;entryInfo:{{apitype|TraitEntryInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| definitionID || {{apitype|number?}} || Nil on SubTreeSelection Node Entries
|-
| subTreeID || {{apitype|number?}} || <font color="green">11.0.0</font> - Populated only on SubTreeSelection Node Entries; This is the SubTree that is activated if this Entry is chosen
|-
| type || {{apitype|Enum.TraitNodeEntryType}} || 
|-
| maxRanks || {{apitype|number}} || 
|-
| isAvailable || {{apitype|boolean}} || Depends on conditions, and is the only reason why configID is required
|-
| isDisplayError || {{apitype|boolean}} || <font color="green">11.0.2</font> - True if this entry fails the TRAIT_CONDITION_TYPE_DISPLAY_ERROR condition check. Used to communicate a problem with the node to the player (e.g. A prerequisite node has not been purchased.) but will not prevent the player from spending points on the node.
|-
| conditionIDs || {{apitype|number[]}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.TraitNodeEntryType
! Value !! Field !! Description
|-
| 0 || SpendHex || 
|-
| 1 || SpendSquare || 
|-
| 2 || SpendCircle || 
|-
| 3 || SpendSmallCircle || 
|-
| 4 || DeprecatedSelect || 
|-
| 5 || DragAndDrop || 
|-
| 6 || SpendDiamond || 
|-
| 7 || ProfPath || 
|-
| 8 || ProfPerk || 
|-
| 9 || ProfPathUnlock || 
|}

{{apinavbox|C_Traits}}
```