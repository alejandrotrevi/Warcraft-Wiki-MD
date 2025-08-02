# API ReforgeItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Reforges the current item, and pays for the cost.
 ReforgeItem(reforgeID)

==Arguments==
:;reforgeID:{{apitype|number}} - [[API GetDestinationReforgeStats|Reforge ID]]

==Returns==
none

* {{api|t=e|FORGE_MASTER_ITEM_CHANGED}}


==Details==
: Using 0 as the Reforge ID will restore the reforge
```