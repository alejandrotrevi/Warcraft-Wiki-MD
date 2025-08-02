# API C Traits.GetTreeNodes

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Returns a list of nodeIDs for a given treeID. For talent trees, this contains nodes for all specializations of the tree's class.
 nodeIDs = C_Traits.GetTreeNodes(treeID)

==Arguments==
:;treeID:{{apitype|number}} - e.g. from {{api|C_Traits.GetConfigInfo}}

==Returns==
:;nodeIDs:{{apitype|number[]}} - list of nodeIDs in ascending order, can be used in {{api|C_Traits.GetNodeInfo}}

{{apinavbox|C_Traits}}
```