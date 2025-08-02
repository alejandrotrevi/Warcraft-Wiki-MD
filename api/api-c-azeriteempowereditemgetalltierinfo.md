# API C AzeriteEmpoweredItem.GetAllTierInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 tierInfo = C_AzeriteEmpoweredItem.GetAllTierInfo(azeriteEmpoweredItemLocation)
          = C_AzeriteEmpoweredItem.GetAllTierInfoByItemID(itemInfo [, classID])

==Arguments==
===<font color="#4ec9b0">GetAllTierInfo</font>===
:;azeriteEmpoweredItemLocation:{{apitype|ItemLocationMixin}}
===<font color="#4ec9b0">GetAllTierInfoByItemID</font>===
:;itemInfo:{{apitype|number,string}} : {{:ItemInfo}}
:;classID:{{apitype|number?}} - Specify a class ID to get tier information about that class, otherwise uses the player's class if left nil

==Returns==
:;tierInfo:structure - AzeriteEmpoweredItemTierInfo[]
{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| azeritePowerIDs || number[] ||
|-
| unlockLevel || number ||
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```