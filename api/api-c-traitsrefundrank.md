# API C Traits.RefundRank

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Attempt to refund a rank. Changes are not applied until they are committed (through {{api|C_Traits.CommitConfig}} or {{api|C_ClassTalents.CommitConfig}}).
 success = C_Traits.RefundRank(configID, nodeID[, clearEdges])

==Arguments==
:;configID:{{apitype|number}}
:;nodeID:{{apitype|number}}
:;clearEdges:{{apitype|boolean?}} if true, refunding the talent will refund all talents that no longer meet their requirements

==Returns==
:;success:{{apitype|boolean}}

==Details==
If you pass clearEdges = true, it's possible that refunding a node results in other nodes being refunded too. E.g. if you no longer meet a gate criterium, or if the node is the only path to a set of selected talents.

==See also==
{{api|C_Traits.SetSelection}} to unselect a Selection node. {{api|C_Traits.RefundRank}} must '''not''' be used with selection nodes (aka choice nodes).

{{apinavbox|C_Traits}}
```