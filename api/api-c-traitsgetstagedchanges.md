# API C Traits.GetStagedChanges

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Returns IDs of Trait Nodes with pending changes, grouped by the type of change; Returns nothing if there are no pending changes
 nodeIDsWithPurchases, nodeIDsWithRefunds, nodeIDsWithSelectionSwaps = C_Traits.GetStagedChanges(configID)

==Arguments==
:;configID:{{apitype|number}}

==Returns==
:;nodeIDsWithPurchases:{{apitype|number[]}}
:;nodeIDsWithRefunds:{{apitype|number[]}}
:;nodeIDsWithSelectionSwaps:{{apitype|number[]}} - Selection nodes that had a previously committed selected entry, and now have a different selected entry pending
```