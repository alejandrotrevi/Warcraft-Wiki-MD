# API IsEquippedItemType

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns true if an item of a given type is equipped.
 isEquipped = IsEquippedItemType(type)

==Arguments==
:;type:{{apitype|string}} ([[ItemType]]) - any valid [[Enum.InventoryType|inventory type]], item class, or item subclass

==Returns==
:;isEquipped:{{apitype|boolean}} - is an item of the given type equipped

==Example==
 if IsEquippedItemType("Shields") then
   DEFAULT_CHAT_FRAME:AddMessage("I have a shield")
 end

<big>'''Result'''</big>

Outputs "I have a shield" to the default chat window if the player has a shield equipped.
```