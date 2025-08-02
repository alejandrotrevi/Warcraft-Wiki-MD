# API GetVoidItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a Void Storage slot.
 itemID, textureName, locked, recentDeposit, isFiltered, quality = GetVoidItemInfo(tabIndex, slotIndex)

==Arguments==
:;tabIndex:{{apitype|number}} - Index ranging from 1 to 2
:;slotIndex:{{apitype|number}} - Index ranging from 1 to [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/AddOns/Blizzard_VoidStorageUI/Blizzard_VoidStorageUI.lua#L8 VOID_STORAGE_MAX]

[[Image:API_GetVoidItemInfo.png|thumb|218px|Bottomleft: locked,<br>Bottomright: recentDeposit]]

==Returns==
:;itemID:{{apitype|number}} - [[API_GetItemInfo|Item ID]]
:;textureName:{{apitype|string}} - Item Icon
:;locked:{{apitype|boolean}} - If the item is locked (e.g. picked up by the mouse cursor)
:;recentDeposit:{{apitype|boolean}} - If the item has been recently deposited (glow effect)
:;isFiltered:{{apitype|boolean}} - If the item is filtered by the search function (greyed/blacked out)
:;quality:{{apitype|number}} - The [[API TYPE Quality|quality]] of the item.  The value is 0 to 7, which represents Poor to Heirloom. This appears to include gains from upgrades/bonuses.

==Example==
70920 {{item|Bracers of the Fiery Path}}
 /dump GetVoidTransferDepositInfo(1)

 => 70920, "Interface\Icons\inv_bracer_plate_raiddeathknight_j_01", false, false, false

==See also==
* {{api|t=w|GetVoidItemHyperlinkString}}
```