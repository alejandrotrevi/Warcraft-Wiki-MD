# API C Traits.SetSelection

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Attempt change the current selection for a selection node (aka choice node). Changes are not applied until they are committed (through {{api|C_Traits.CommitConfig}} or {{api|C_ClassTalents.CommitConfig}}).
 success = C_Traits.SetSelection(configID, nodeID [, nodeEntryID[, clearEdges]])

==Arguments==
:;configID:{{apitype|number}}
:;nodeID:{{apitype|number}}
:;nodeEntryID:{{apitype|number?}} pass nil to unselect the node, effectively the equivalent of {{api|C_Traits.RefundRank}}.
:;clearEdges:{{apitype|boolean?}} if true, unselecting the node will refund all talents that no longer meet their requirements

==Returns==
:;success:{{apitype|boolean}}

==Details==
This API can be used to set the initial selection, change a selection, or unselect a selection node (aka choice node). Passing clearEdges = true, and unselecting a selection node, may result in other talents being refunded, e.g. if you no longer meet a gate criterium, or if the selection node is the only path to a set of selected talents.

You should not use the {{api|C_Traits.PurchaseRank}} or {{api|C_Traits.RefundRank}} APIs on selection nodes. {{api|C_Traits.SetSelection}} is the only API used to modify selection node choices.

{{apinavbox|C_Traits}}
```