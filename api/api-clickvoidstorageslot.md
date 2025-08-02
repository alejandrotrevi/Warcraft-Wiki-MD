# API ClickVoidStorageSlot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Clicks the specified Void Storage slot.
 ClickVoidStorageSlot(slotIndex[, isRightClick])

==Arguments==
:;slotIndex:{{apitype|number}} - Index ranging from 1 to [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/AddOns/Blizzard_VoidStorageUI/Blizzard_VoidStorageUI.lua#L8 VOID_STORAGE_MAX].
:;isRightClick:{{apitype|boolean?}} - Whether the button was right-clicked.

==Triggers events==
* {{api|t=e|VOID_STORAGE_CONTENTS_UPDATE}}

==Details==
* Left-click (false): Toggles the item between the specified button and the mouse cursor
* Right-click (true): Sets the item for withdrawal
```