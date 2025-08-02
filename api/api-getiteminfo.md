# API GetItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns info for an item.
 itemName, itemLink, itemQuality, itemLevel, itemMinLevel, itemType, itemSubType, itemStackCount, itemEquipLoc, itemTexture, sellPrice, classID, subclassID, bindType, expansionID, setID, isCraftingReagent = GetItemInfo(itemInfo)

==Arguments==
:;item:{{apitype|ItemInfo}}

==Returns==
:;1. itemName:{{apitype|string}}
:;2. itemLink:{{apitype|string}}
:;3. itemQuality:{{apitype|number}}
:;4. itemLevel:{{apitype|number}}
:;5. itemMinLevel:{{apitype|number}}
:;6. itemType:{{apitype|string}}
:;7. itemSubType:{{apitype|string}}
:;8. itemStackCount:{{apitype|number}}
:;9. itemEquipLoc:{{apitype|string}}
:;10. itemTexture:{{apitype|number}}
:;11. sellPrice:{{apitype|number}}
:;12. classID:{{apitype|number}}
:;13. subclassID:{{apitype|number}}
:;14. bindType:{{apitype|number}}
:;15. expansionID:{{apitype|number}}
:;16. setID:{{apitype|number?}}
:;17. isCraftingReagent:{{apitype|boolean}}

==Patch changes==
* {{Patch 10.2.6|note=Namespaced to <code>C_Item.GetItemInfo</code>.}}
```