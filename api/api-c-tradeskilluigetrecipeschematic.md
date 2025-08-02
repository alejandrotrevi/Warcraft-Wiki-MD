# API C TradeSkillUI.GetRecipeSchematic

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Needs summary.
 schematic = C_TradeSkillUI.GetRecipeSchematic(recipeSpellID, isRecraft [, recipeLevel])

==Arguments==
:;recipeSpellID:{{apitype|number}}
:;isRecraft:{{apitype|boolean}}
:;recipeLevel:{{apitype|number?}}

==Returns==
:;schematic:{{apitype|CraftingRecipeSchematic}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|recipeID}} || {{apitype|number}} || 
|-
| {{apiname|icon}} || {{apitype|number}} || 
|-
| {{apiname|quantityMin}} || {{apitype|number}} || 
|-
| {{apiname|quantityMax}} || {{apitype|number}} || 
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|recipeType}} || {{apitype|Enum.TradeskillRecipeType?|default=Item}} || 
|-
| {{apiname|productQuality}} || {{apitype|number?}} || 
|-
| {{apiname|outputItemID}} || {{apitype|number?}} || 
|-
| {{apiname|reagentSlotSchematics}} || {{apitype|CraftingReagentSlotSchematic[]}} || 
|-
| {{apiname|isRecraft}} || {{apitype|boolean}} || 
|-
| {{apiname|hasCraftingOperationInfo}} || {{apitype|boolean}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.TradeskillRecipeType
! Value !! Field !! Description
|-
| 1 || {{apiname|Item}} || 
|-
| 2 || {{apiname|Salvage}} || 
|-
| 3 || {{apiname|Enchant}} || 
|-
| 4 || {{apiname|Recraft}} || 
|-
| 5 || {{apiname|Gathering}} || <font color="green">10.0.5</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ CraftingReagentSlotSchematic
! Field !! Type !! Description
|-
| {{apiname|reagents}} || {{apitype|CraftingReagent[]}} || 
|-
| {{apiname|reagentType}} || {{apitype|Enum.CraftingReagentType}} || 
|-
| {{apiname|quantityRequired}} || {{apitype|number}} || 
|-
| {{apiname|slotInfo}} || {{apitype|CraftingReagentSlotInfo?}} || 
|-
| {{apiname|dataSlotType}} || {{apitype|Enum.TradeskillSlotDataType?|default=Reagent}} || 
|-
| {{apiname|dataSlotIndex}} || {{apitype|number}} || 
|-
| {{apiname|slotIndex}} || {{apitype|number}} || 
|-
| {{apiname|orderSource}} || {{apitype|Enum.CraftingOrderReagentSource?}} || 
|-
| {{apiname|required}} || {{apitype|boolean}} || <font color="green">10.1.0</font>
|-
| {{apiname|hiddenInCraftingForm}} || {{apitype|boolean}} || <font color="green">11.2.0</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ CraftingReagent
! Field !! Type !! Description
|-
| {{apiname|itemID}} || {{apitype|number?}} || 
|-
| {{apiname|currencyID}} || {{apitype|number?}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.CraftingReagentType
! Value !! Field !! Description
|-
| 0 || {{apiname|Modifying}} || <font color="green">10.1.0</font> - Renamed from <code>Optional</code>
|-
| 1 || {{apiname|Basic}} || 
|-
| 2 || {{apiname|Finishing}} || 
|-
| 3 || {{apiname|Automatic}} || <font color="green">10.1.0</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ CraftingReagentSlotInfo
! Field !! Type !! Description
|-
| {{apiname|mcrSlotID}} || {{apitype|number}} || 
|-
| {{apiname|requiredSkillRank}} || {{apitype|number}} || 
|-
| {{apiname|slotText}} || {{apitype|string?}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.TradeskillSlotDataType
! Value !! Field !! Description
|-
| 1 || {{apiname|Reagent}} || 
|-
| 2 || {{apiname|ModifiedReagent}} || 
|-
| 3 || {{apiname|Currency}} || 
|}

{{:Enum.CraftingOrderReagentSource}}

==Patch changes==
* {{Patch 10.0.5|note=Removed <code>hasGatheringOperationInfo</code> field.}}
```