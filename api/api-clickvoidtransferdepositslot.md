# API ClickVoidTransferDepositSlot

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Clicks the specified Void Transfer deposit slot.
 ClickVoidTransferDepositSlot(slotIndex [, isRightClick])

==Arguments==
:;slotIndex:{{apitype|number}} - Index ranging from 1 to [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/AddOns/Blizzard_VoidStorageUI/Blizzard_VoidStorageUI.lua#L6 VOID_DEPOSIT_MAX]. Defaults to 1 if not a valid Index.
:;isRightClick:{{apitype|boolean?}} - Whether the button was right-clicked

==Triggers events==
* {{api|t=e|VOID_STORAGE_DEPOSIT_UPDATE}}


==Details==
* Left-click (false): Toggles the item between the specified button and the mouse cursor
* Right-click (true): Removes the item from the specified button
```