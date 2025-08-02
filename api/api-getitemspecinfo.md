# API GetItemSpecInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns which specializations an item is useful for.
 specTable = GetItemSpecInfo(itemLink or itemID or itemName [, specTable])

==Arguments==
:;itemLink or itemID or itemName:Mixed : link, id, or name of the item to query.
:;specTable:{{apitype|table}} - if provided, this table will be populated with the results and returned; otherwise, a new table will be created.

==Returns==
:;specTable:{{apitype|table}} - if the item is flagged as being for specific specializations, an array containing the [[SpecializationID|SpecializationIDs]] of specializations of the player's class for which the queried item is suitable; nil if information is unavailable.

==Details==
* The supplied <code>specTable</code> is not wiped; only the array keys necessary to return the result are modified.
* Spec information is only available for some items.
* The returned specialization IDs are not sorted. You can use <code>[[API sort|table.sort]]</code> to bring them into the same order as the Specialization pane displays.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|GetSpecializationInfoByID}}
```