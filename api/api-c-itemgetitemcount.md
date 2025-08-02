# API C Item.GetItemCount

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Returns the number (or available charges) of an item in the inventory.
 count = C_Item.GetItemCount(itemInfo [, includeBank [, includeUses [, includeReagentBank [, includeAccountBank]]]])

==Arguments==
:;itemInfo:{{apitype|ItemInfo}}
:;includeBank:{{apitype|boolean?|default=false}}
:;includeUses:{{apitype|boolean?|default=false}}
:;includeReagentBank:{{apitype|boolean?|default=false}}
:;includeAccountBank:{{apitype|boolean?|default=false}}

==Returns==
:;count:{{apitype|number}}

==Patch changes==
* {{Patch 11.0.0|note=Added <code>includeAccountBank</code> parameter.}}
```