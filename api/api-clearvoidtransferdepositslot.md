# API ClearVoidTransferDepositSlot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Clears the specified Void Transfer deposit slot.
 ClearVoidTransferDepositSlot(slotIndex)

==Arguments==
:;slotIndex:{{apitype|number}} - Index ranging from 1 to [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/AddOns/Blizzard_VoidStorageUI/Blizzard_VoidStorageUI.lua#L6 VOID_DEPOSIT_MAX]

==Triggers events==
* {{api|t=e|VOID_STORAGE_DEPOSIT_UPDATE}}

==Details==
* This used when declining the confirmation window on {{api|t=e|VOID_DEPOSIT_WARNING}}.

[[Image:EVENT_VOID_DEPOSIT_WARNING.png|thumb|VOID_DEPOSIT_WARNING]]
```