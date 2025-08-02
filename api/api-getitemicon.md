# API GetItemIcon

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the icon texture for an item.
 icon = GetItemIcon(itemID) 

==Arguments==
:;itemID:{{apitype|number}} - The ID of the item to query e.g. 23405 for [[Farstrider's Tunic]].

==Returns==
:;icon:{{apitype|number}} : [[FileID]] - Icon texture used by the item.

==Details==
* Unlike {{api|GetItemInfo}}(), this function does not require the item to be readily available from the item cache.
```