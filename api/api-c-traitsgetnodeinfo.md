# API C Traits.GetNodeInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Returns NodeInfo applicable to the configID you enter.
 nodeInfo = C_Traits.GetNodeInfo(configID, nodeID)

==Arguments==
:;configID:{{apitype|number}} - For TalentTrees this will often be {{api|C_ClassTalents.GetActiveConfigID}}, this is -1 when inspecting a player. For professions, this will be {{api|C_ProfSpecs.GetConfigIDForSkillLine}}. See also <code>Constants.TraitConsts</code> for a few special ConfigIDs.
:;nodeID:{{apitype|number}} - e.g. from {{api|C_Traits.GetTreeNodes}}

==Returns==
:;nodeInfo:{{apitype|TraitNodeInfo?}} - if the configID is not valid, returns nil. If information for a node cannot be retrieved for another reason, all fields are zeroed out. Most information relates to your current '''preview''' state, unless otherwise specified
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| ID || {{apitype|number}} || nodeID, 0 if node information isn't available to you
|-
| posX || {{apitype|number}} || X offset relative to the topleft corner of the UI, some class talent trees have an additional global offset
|-
| posY || {{apitype|number}} || Y offset relative to the topleft corner of the UI, some class talent trees have an additional global offset
|-
| flags || {{apitype|number}} || &1: ShowMultipleIcons - generally 0 for regular nodes, 1 for choice nodes
|-
| entryIDs || {{apitype|number[]}} || List of entryIDs - generally there is 1 for regular nodes, 2 for choice nodes; used in {{api|C_Traits.GetEntryInfo}}
|-
| entryIDsWithCommittedRanks || {{apitype|number[]}} || '''Committed''' entryIDs, which can be different from the preview state. E.g. moving talents/traits around, without pressing the confirm button, will not change this value
|-
| canPurchaseRank || {{apitype|boolean}} || False if you already have the max ranks purchased / granted; true otherwise
|-
| canRefundRank || {{apitype|boolean}} || False if you purchased 0 ranks; true otherwise
|-
| isAvailable || {{apitype|boolean}} || False if not available due to Gates (i.e. you may need to spend x more points to unlock a new row of traits/talents)
|-
| isVisible || {{apitype|boolean}} || False if a node should not be shown in the UI, this generally only happens when all other info is zeroed out as well
|-
| isDisplayError || {{apitype|boolean}} || <font color="green">11.0.2</font> - True if this node fails the TRAIT_CONDITION_TYPE_DISPLAY_ERROR condition check. Used to communicate a problem with the node to the player (e.g. A prerequisite node has not been purchased.) but will not prevent the player from spending points on the node
|-
| ranksPurchased || {{apitype|number}} || Number of ranks '''purchased''', automatically granted ranks do not count
|-
| activeRank || {{apitype|number}} || The current (preview) rank for the node - used to track if the node is maxed, or has progress; this can never be greater than maxRanks
|-
| currentRank || {{apitype|number}} || Similar to activeRank - used for tooltips and other texts; through bugs, it can be possible for this to be greater than maxRanks, seems to be the sum of GrantedRanks + PurchasedRanks
|-
| activeEntry || {{apitype|TraitEntryRankInfo?}} || The currently selected (preview) entry; if no entry is learned, regular nodes have an entry with rank 0, choice nodes have nil; the rank matches activeRank
|-
| nextEntry || {{apitype|TraitEntryRankInfo?}} || The next entry when spending a point; nil for choice nodes, or if maxed
|-
| maxRanks || {{apitype|number}} || Maximum ranks for a node, also applies to choice nodes
|-
| type || {{apitype|Enum.TraitNodeType}} || The type of node, has implications for how the API interacts with the node, and how the UI displays and interacts with the node
|-
| visibleEdges || {{apitype|TraitOutEdgeInfo[]}} || Outgoing connections for a node, filtered to only return edges with a visible target node - the UI displays these as arrows pointing towards other nodes
|-
| meetsEdgeRequirements || {{apitype|boolean}} || True if incoming edge requirements are met (see Enum.TraitEdgeType), or if there are no incoming edges (i.e. the initial nodes in a tree), false otherwise - the UI uses this to disable the node button
|-
| groupIDs || {{apitype|number[]}} || TraitNodeGroups are not generally exposed through the API, but they relate to how Gates work, TraitCurrency costs, TraitConditions, and possibly more
|-
| conditionIDs || {{apitype|number[]}} || Can be used for {{api|C_Traits.GetConditionInfo}} conditions can grant ranks, limit visibility to specs, set Gate requirements, and more
|-
| isCascadeRepurchasable || {{apitype|boolean}} || If true, you can shift-click to purchase back nodes that you previously had selected, but were deselected because you unlearned something higher up in the tree
|-
| cascadeRepurchaseEntryID || {{apitype|number?}} || 
|-
| subTreeID || {{apitype|number?}} || <font color="green">11.0.0</font> - The SubTree this Node belongs to; Nil if it is not part of a SubTree
|-
| subTreeActive || {{apitype|boolean?}} || <font color="green">11.0.0</font> - True if this node has a SubTreeID, and the SubTree is chosen or staged; May be nil if not part of a SubTree at all
|}

{{:Struct TraitEntryRankInfo}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.TraitNodeType
! Value !! Field !! Description
|-
| 0 || {{apiname|Single}} || The most common type, includes multi-rank traits and single-rank traits
|-
| 1 || {{apiname|Tiered}} || Unsure where this is used, but seems to result in the node and nodeEntry costs being combined in some way
|-
| 2 || {{apiname|Selection}} || Applies to all choice nodes, where you can select between multiple (generally 2) options
|-
| 3 || {{apiname|SubTreeSelection}} || <font color="green">11.0.0</font>
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ style="text-align:left; margin-left: 2em" | TraitOutEdgeInfo
! Field !! Type !! Description
|-
| targetNode || {{apitype|number}} || The target nodeID
|-
| type || {{apitype|Enum.TraitEdgeType}} || Has implications on how meetsEdgeRequirements is calculated
|-
| visualStyle || {{apitype|Enum.TraitEdgeVisualStyle}} || Defines how the UI displays the edge
|-
| isActive || {{apitype|boolean}} || Active edges generally have a different visual, and meetsEdgeRequirements is calculated based on active incoming edges
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ style="text-align:left; margin-left: 2em" | Enum.TraitEdgeType
! Value !! Field !! Description
|-
| 0 || VisualOnly || Simply results in a visual connection, has no impact on edge requirements
|-
| 1 || DeprecatedRankConnection || Presumably deprecated, and can be ignored
|-
| 2 || SufficientForAvailability || If any incoming edge of this type is active, all edges of this type pass the edge requirements
|-
| 3 || RequiredForAvailability || All incoming edges of this type must be active to pass the edge requirements
|-
| 4 || MutuallyExclusive || No edges of this type currently exist, but the UI does show a different visual effect - presumably, only 1 incoming edge if this type is allowed to be active, to pass the edge requirements
|-
| 5 || DeprecatedSelectionOption || Presumably deprecated, and can be ignored
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ style="text-align:left; margin-left: 2em" | Enum.TraitEdgeVisualStyle
! Value !! Field !! Description
|-
| 0 || None || No edges of this type exist, presumably, they would not display in the UI
|-
| 1 || Straight || A simple straight arrow between nodes
|}

{{apinavbox|C_Traits}}
```