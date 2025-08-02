# API C Traits.PurchaseRank

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Attempt to purchase a rank. Changes are not applied until they are committed (through {{api|C_Traits.CommitConfig}} or {{api|C_ClassTalents.CommitConfig}}).
 success = C_Traits.PurchaseRank(configID, nodeID)

==Arguments==
:;configID:{{apitype|number}}
:;nodeID:{{apitype|number}}

==Returns==
:;success:{{apitype|boolean}}

==See also==
{{api|C_Traits.SetSelection}} to purchase/select a Selection node. {{api|C_Traits.PurchaseRank}} should '''not''' be used with selection nodes (aka choice nodes).

{{apinavbox|C_Traits}}
```