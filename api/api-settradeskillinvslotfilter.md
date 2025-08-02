# API SetTradeSkillInvSlotFilter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Set the inventory slot type filter.
 SetTradeSkillInvSlotFilter(slotIndex, onOff{, exclusive} )

----
;''Arguments''

: Number slotIndex, Boolean onOff, Boolean exclusive

:;slotIndex:The index of the specific slot

:;onOff:On = true, Off = false

:;exclusive(Optional):Sets if the slot is the only slot to be selected. If not set it's handled as Off. On = true, Off = false

----
;''Returns''

: nil

----
;''Example''

Sets the filter to select slotIndex 3 and 5. First slotIndex have to be exclusive enabled.
 SetTradeSkillInvSlotFilter(3, 1, 1);
 SetTradeSkillInvSlotFilter(5, 1);

==See Also==
[[API_GetTradeSkillInvSlotFilter|GetTradeSkillInvSlotFilter]]
```