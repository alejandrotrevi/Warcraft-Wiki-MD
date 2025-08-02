# API GetVoidTransferWithdrawalInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
 {{wowapi}}
Returns info for the item being withdrawn from the Void Storage.
 itemID, textureName = GetVoidTransferWithdrawalInfo(slotIndex)

==Arguments==
:;slotIndex:{{apitype|number}} - Index ranging from 1 to [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/AddOns/Blizzard_VoidStorageUI/Blizzard_VoidStorageUI.lua#L7 VOID_WITHDRAW_MAX]

==Returns==
:;itemID:{{apitype|number}} - [[API_GetItemInfo|Item ID]]
:;textureName:{{apitype|string}} - Item Icon

[[Image:API_GetVoidTransferWithdrawalInfo.png|thumb|220px]]

==Example==
70920 {{item|Bracers of the Fiery Path}}
 /dump GetVoidTransferWithdrawalInfo(1)

 => 70920, "Interface\Icons\inv_bracer_plate_raiddeathknight_j_01"
```