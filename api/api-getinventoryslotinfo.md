# API GetInventorySlotInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an equipment slot.
 invSlotId, textureName, checkRelic = GetInventorySlotInfo(invSlotName)

==Arguments==
:;invSlotName:{{apitype|string}} - [[InventorySlotId|InventorySlotName]] to query (e.g. "HEADSLOT").

==Returns==
:;invSlotId:{{apitype|number}} : [[InventorySlotId]] - The ID to use to refer to that slot in the other GetInventory functions.
:;textureName:{{apitype|string}} - The texture to use for the empty slot on the paper doll display.
:;checkRelic:{{apitype|boolean}}
<!-- luals
---@param invSlotName InventorySlotName 
---@return number invSlotId
---@return string textureName
---@return boolean checkRelic
function GetInventorySlotInfo(invSlotName) end
-->
```