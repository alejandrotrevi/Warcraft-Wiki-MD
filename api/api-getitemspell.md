# API GetItemSpell

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the spell effect for an item.
 spellName, spellID = GetItemSpell(itemID or itemString or itemName or itemLink)

==Arguments==
One of the following four ways to specify which item to query:
:;itemId:{{apitype|number}} - Numeric ID of the item.
:;itemName:{{apitype|string}} - Name of an item owned by the player at some point during this session.
:;itemString:{{apitype|string}} - A fragment of the [[itemString]] for the item, e.g. "item:30234:0:0:0:0:0:0:0" or "item:30234".
:;itemLink:{{apitype|string}} - The full [[itemLink]].

==Returns==
:;spellName:{{apitype|string}} - The name of the spell.
:;spellID:{{apitype|number}} - The spell's unique identifier.

==Details==
* Useful for determining whether an item is usable.
```