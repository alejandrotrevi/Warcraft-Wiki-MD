# API C Container.GetContainerNumFreeSlots

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Container|system=Container}}
Returns the number of free slots & the bagType that an equipped bag or backpack belongs to.
 numFreeSlots, bagType = C_Container.GetContainerNumFreeSlots(bagIndex)

==Arguments==
:;bagIndex:{{apitype|number}}

==Returns==
:;numFreeSlots:{{apitype|number}}
:;bagType:{{apitype|number}} : [[ItemFamily]]

==See also==
*{{api|GetItemFamily}} - Returns bagType of item.
```