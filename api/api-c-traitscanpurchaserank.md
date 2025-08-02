# API C Traits.CanPurchaseRank

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Checks whether a node entry is purchasable.
 canPurchase = C_Traits.CanPurchaseRank(configID, nodeID, nodeEntryID)

==Arguments==
:;configID:{{apitype|number}}
:;nodeID:{{apitype|number}}
:;nodeEntryID:{{apitype|number}}

==Returns==
:;canPurchase:{{apitype|boolean}}

==Details==
There is generally little value in calling this API, instead, you can call {{api|C_Traits.PurchaseRank}} or {{api|C_Traits.SetSelection}} directly, and check their return values.

Currently, the default UI only uses this API for profession nodes, to check whether unlocking a node, or spending points on the node is possible, and not for generic talents or class talents.

{{apinavbox|C_Traits}}
```