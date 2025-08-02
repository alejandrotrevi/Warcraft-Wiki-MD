# API C Traits.ResetTreeByCurrency

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Resets the tree, refunding any purchased traits where possible, but only if the trait costs the specified traitCurrencyID
 success = C_Traits.ResetTreeByCurrency(configID, treeID, traitCurrencyID)

==Arguments==
:;configID:{{apitype|number}}
:;treeID:{{apitype|number}}
:;traitCurrencyID:{{apitype|number}}

==Returns==
:;success:{{apitype|boolean}}

==Details==
This API is used to reset only class talents, or only spec talents, rather than resetting the entire tree with {{api|C_Traits.ResetTree}}.

{{apinavbox|C_Traits}}
```