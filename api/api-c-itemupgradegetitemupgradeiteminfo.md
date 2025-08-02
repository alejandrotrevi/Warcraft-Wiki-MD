# API C ItemUpgrade.GetItemUpgradeItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ItemUpgrade|system=ItemUpgrade}}
Needs summary.
 itemInfo = C_ItemUpgrade.GetItemUpgradeItemInfo()

==Returns==
:;itemInfo:{{apitype|ItemUpgradeItemInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| iconID || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| itemUpgradeable || {{apitype|boolean}} || 
|-
| displayQuality || {{apitype|number}} || 
|-
| highWatermarkSlot || {{apitype|number}} || <font color="green">10.1.0</font>
|-
| currUpgrade || {{apitype|number}} || 
|-
| maxUpgrade || {{apitype|number}} || 
|-
| minItemLevel || {{apitype|number}} || <font color="green">10.1.0</font>
|-
| maxItemLevel || {{apitype|number}} || <font color="green">10.1.0</font>
|-
| upgradeLevelInfos || {{apitype|ItemUpgradeLevelInfo[]}} || 
|-
| customUpgradeString || {{apitype|string?}} || <font color="green">10.1.0</font>
|-
| upgradeCostTypesForSeason || {{apitype|ItemUpgradeSeasonalCostType[]}} || <font color="green">10.1.0</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ ItemUpgradeLevelInfo
! Field !! Type !! Description
|-
| upgradeLevel || {{apitype|number}} || 
|-
| displayQuality || {{apitype|number}} || 
|-
| itemLevelIncrement || {{apitype|number}} || 
|-
| levelStats || {{apitype|ItemUpgradeStat[]}} || 
|-
| currencyCostsToUpgrade || {{apitype|ItemUpgradeCurrencyCost[]}} || <font color="green">10.0.5</font>
|-
| itemCostsToUpgrade || {{apitype|ItemUpgradeItemCost[]}} || <font color="green">10.0.5</font>
|-
| failureMessage || {{apitype|string?}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ ItemUpgradeStat
! Field !! Type !! Description
|-
| displayString || {{apitype|string}} || 
|-
| statValue || {{apitype|number}} || 
|-
| active || {{apitype|boolean}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ ItemUpgradeCurrencyCost
! Field !! Type !! Description
|-
| cost || {{apitype|number}} || 
|-
| currencyID || {{apitype|number}} || 
|-
| discountInfo || {{apitype|ItemUpgradeCostDiscountInfo}} || <font color="green">10.1.0</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ ItemUpgradeItemCost
! Field !! Type !! Description
|-
| cost || {{apitype|number}} || 
|-
| itemID || {{apitype|number}} || 
|-
| discountInfo || {{apitype|ItemUpgradeCostDiscountInfo}} || <font color="green">10.1.0</font>
|}

{{:Struct ItemUpgradeCostDiscountInfo}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ ItemUpgradeSeasonalCostType
! Field !! Type !! Description
|-
| itemID || {{apitype|number}} || 
|-
| orderIndex || {{apitype|number}} || 
|-
| sourceString || {{apitype|string?}} || 
|}

==Patch changes==
* {{Patch 10.0.5|note=Removed <code>costsToUpgrade</code> field.}}
* {{Patch 9.1.5|note=Added.}}
```