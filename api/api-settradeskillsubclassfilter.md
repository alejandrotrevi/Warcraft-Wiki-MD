# API SetTradeSkillSubClassFilter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the subclass filter.
 SetTradeSkillSubClassFilter(slotIndex, onOff{, exclusive})

==Arguments==
:;slotIndex:The index of the specific slot
:;onOff:On = 1, Off = 0
:;exclusive(Optional):Sets if the slot is the only slot to be selected. If not set it's handled as Off. On = 1, Off = 0

==Example==
Sets the filter to select slotIndex 3 and 5. First slotIndex have to be exclusive enabled.
 SetTradeSkillSubClassFilter(3, 1, 1);
 SetTradeSkillSubClassFilter(5, 1);

==Patch changes==
* {{Patch 5.0.4|note=Removed.}}

==See Also==
[[API GetTradeSkillSubClassFilter|GetTradeSkillSubClassFilter]]
```