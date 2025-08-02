# API C NewItems.IsNewItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the item in the inventory slot is flagged as new.
 isNew = C_NewItems.IsNewItem(containerIndex, slotIndex)

==Arguments==
:;containerIndex:{{apitype|number}} - [[BagID]] of the container.
:;slotIndex:{{apitype|number}} - {{api|t=w|Frame GetID|ID}} of the inventory slot within the container.

==Returns==
:;isNew:{{apitype|boolean}} - Returns true if the inventory slot holds a newly-acquired item; otherwise false (empty slot or a non-new item).

==Patch changes==
* {{Patch 5.4.0|note=Added.<ref name="5.4.0">{{ref FrameXML|ContainerFrame.lua|5.4.0|17359|330|20130909}}</ref>}}

==See also==
* {{api|C_NewItems.RemoveNewItem(bag, slot)}} - Used by <code>FrameXML/ContainerFrame.lua</code> to clear the new-item flag after interacting with the new item or closing the bags.
* {{api|IsBattlePayItem(bag, slot)}} - Used by <code>FrameXML/ContainerFrame.lua</code> to emphasise recent purchases from the [[In-Game Store]].<ref name="6.0.2">{{ref FrameXML|ContainerFrame.lua|6.0.2|19033|330|20130909}}</ref>

==References==
{{Reflist}}
```