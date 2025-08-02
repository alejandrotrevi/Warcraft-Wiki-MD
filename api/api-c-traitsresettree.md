# API C Traits.ResetTree

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Resets the tree, refunding any purchased traits where possible. The reset is '''not''' automatically saved, use {{api|C_Traits.CommitConfig}} for that.
 success = C_Traits.ResetTree(configID, treeID)

==Arguments==
:;configID:{{apitype|number}}
:;treeID:{{apitype|number}}

==Returns==
:;success:{{apitype|boolean}}

{{apinavbox|C_Traits}}
```