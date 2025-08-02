# API C PlayerChoice.GetCurrentPlayerChoiceInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PlayerChoice|system=PlayerChoice}}
Needs summary.
 choiceInfo = C_PlayerChoice.GetCurrentPlayerChoiceInfo()

==Returns==
:;choiceInfo:{{apitype|PlayerChoiceInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|objectGUID}} || {{apitype|WOWGUID}} || 
|-
| {{apiname|choiceID}} || {{apitype|number}} || 
|-
| {{apiname|questionText}} || {{apitype|string}} || 
|-
| {{apiname|pendingChoiceText}} || {{apitype|string}} || 
|-
| {{apiname|uiTextureKit}} || {{apitype|textureKit}} || 
|-
| {{apiname|hideWarboardHeader}} || {{apitype|boolean}} || 
|-
| {{apiname|keepOpenAfterChoice}} || {{apitype|boolean}} || 
|-
| {{apiname|showChoicesAsList}} || {{apitype|boolean}} || 
|-
| {{apiname|options}} || {{apitype|PlayerChoiceOptionInfo[]}} || 
|-
| {{apiname|soundKitID}} || {{apitype|number?}} || 
|-
| {{apiname|closeUISoundKitID}} || {{apitype|number?}} || 
|}

{| class="vertical-align-row"
|
    {| class="sortable darktable zebra" style="margin-left: 3.9em"
    |+ PlayerChoiceOptionInfo
    ! Field !! Type !! Description
    |-
    | {{apiname|id}} || {{apitype|number}} || 
    |-
    | {{apiname|description}} || {{apitype|string}} || 
    |-
    | {{apiname|header}} || {{apitype|string}} || 
    |-
    | {{apiname|choiceArtID}} || {{apitype|number}} || 
    |-
    | {{apiname|desaturatedArt}} || {{apitype|boolean}} || 
    |-
    | {{apiname|disabledOption}} || {{apitype|boolean}} || 
    |-
    | {{apiname|hasRewards}} || {{apitype|boolean}} || 
    |-
    | {{apiname|rewardInfo}} || {{apitype|PlayerChoiceOptionRewardInfo}} || 
    |-
    | {{apiname|uiTextureKit}} || {{apitype|textureKit}} || 
    |-
    | {{apiname|maxStacks}} || {{apitype|number}} || 
    |-
    | {{apiname|buttons}} || {{apitype|PlayerChoiceOptionButtonInfo[]}} || 
    |-
    | {{apiname|widgetSetID}} || {{apitype|number?}} || 
    |-
    | {{apiname|spellID}} || {{apitype|number?}} || 
    |-
    | {{apiname|rarity}} || {{apitype|Enum.PlayerChoiceRarity?}} || 
    |-
    | {{apiname|typeArtID}} || {{apitype|number?}} || 
    |-
    | {{apiname|headerIconAtlasElement}} || {{apitype|string?}} || 
    |-
    | {{apiname|subHeader}} || {{apitype|string?}} || 
    |-
    | {{apiname|consolidateWidgets}} || {{apitype|boolean}} || <font color="green">11.0.2</font>
    |}
|
	{| class="sortable darktable zebra" style="margin-left: 3.9em"
	|+ PlayerChoiceOptionRewardInfo
	! Field !! Type !! Description
	|-
	| currencyRewards || {{apitype|PlayerChoiceRewardCurrencyInfo[]}} || 
	|-
	| itemRewards || {{apitype|PlayerChoiceRewardItemInfo[]}} || 
	|-
	| repRewards || {{apitype|PlayerChoiceRewardReputationInfo[]}} || 
	|}

	{| class="sortable darktable zebra" style="margin-left: 3.9em"
	|+ PlayerChoiceRewardCurrencyInfo
	! Field !! Type !! Description
	|-
	| currencyId || {{apitype|number}} || 
	|-
	| name || {{apitype|string}} || 
	|-
	| currencyTexture || {{apitype|number}} || 
	|-
	| quantity || {{apitype|number}} || 
	|-
	| isCurrencyContainer || {{apitype|boolean}} || 
	|}

	{| class="sortable darktable zebra" style="margin-left: 3.9em"
	|+ PlayerChoiceRewardItemInfo
	! Field !! Type !! Description
	|-
	| itemId || {{apitype|number}} || 
	|-
	| name || {{apitype|string}} || 
	|-
	| quantity || {{apitype|number}} || 
	|}

	{| class="sortable darktable zebra" style="margin-left: 3.9em"
	|+ PlayerChoiceRewardReputationInfo
	! Field !! Type !! Description
	|-
	| factionId || {{apitype|number}} || 
	|-
	| quantity || {{apitype|number}} || 
	|}
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.PlayerChoiceRarity
! Value !! Field !! Description
|-
| 0 || {{apiname|Common}} || 
|-
| 1 || {{apiname|Uncommon}} || 
|-
| 2 || {{apiname|Rare}} || 
|-
| 3 || {{apiname|Epic}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ PlayerChoiceOptionButtonInfo
! Field !! Type !! Description
|-
| {{apiname|id}} || {{apitype|number}} || 
|-
| {{apiname|text}} || {{apitype|string}} || 
|-
| {{apiname|disabled}} || {{apitype|boolean}} || 
|-
| {{apiname|showCheckmark}} || {{apitype|boolean}} || 
|-
| {{apiname|hideButtonShowText}} || {{apitype|boolean}} || <font color="green">11.1.7</font>
|-
| {{apiname|selected}} || {{apitype|boolean}} || 
|-
| {{apiname|confirmation}} || {{apitype|string?}} || 
|-
| {{apiname|tooltip}} || {{apitype|string?}} || 
|-
| {{apiname|rewardQuestID}} || {{apitype|number?}} || 
|-
| {{apiname|soundKitID}} || {{apitype|number?}} || 
|-
| {{apiname|listText}} || {{apitype|string?}} || 
|}

==Patch changes==
* {{Patch 11.1.5|note=Removed <code>rarityColor</code> field.}}
* {{Patch 9.2.0|note=Added <code>pendingChoiceText, closeUISoundKitID</code> fields.}}
* {{Patch 9.1.5|note=Added <code>objectGUID</code> field.}}
* {{Patch 9.1.0|note=Added <code>rewardInfo, buttons</code> and <code>isCurrencyContainer</code> fields.}}
* {{Patch 9.1.0|note=Added. Replaces {{api|C_PlayerChoice.GetPlayerChoiceInfo}}, {{api|C_PlayerChoice.GetPlayerChoiceOptionInfo}} and {{api|C_PlayerChoice.GetPlayerChoiceRewardInfo}}}}
```