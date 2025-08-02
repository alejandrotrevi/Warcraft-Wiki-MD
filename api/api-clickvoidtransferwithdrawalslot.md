# API ClickVoidTransferWithdrawalSlot

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Clicks the specified Void Transfer withdrawal slot.
 ClickVoidTransferWithdrawalSlot(slotIndex [, isRightClick])

==Arguments==
:;slotIndex:{{apitype|number}} - Index ranging from 1 to [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/AddOns/Blizzard_VoidStorageUI/Blizzard_VoidStorageUI.lua#L7 VOID_WITHDRAW_MAX].
:;isRightClick:{{apitype|boolean?}} - Whether the button was right-clicked.

==Triggers events==
* {{api|t=e|VOID_STORAGE_CONTENTS_UPDATE}}

==Details==
* Left-click (false): Toggles the item between the specified button and the mouse cursor
* Right-click (true): Cancels withdrawing; Sets the item back into the Void Storage
```