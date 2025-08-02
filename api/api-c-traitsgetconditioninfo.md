# API C Traits.GetConditionInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Returns conditionInfo applicable to the configID you enter
 condInfo = C_Traits.GetConditionInfo(configID, condID)

==Arguments==
:;configID:{{apitype|number}} - For TalentTrees this will often be {{api|C_ClassTalents.GetActiveConfigID}}, this is -1 when inspecting a player. For professions, this will be {{api|C_ProfSpecs.GetConfigIDForSkillLine}}.
:;condID:{{apitype|number}} - trait conditionId as found in e.g. {{api|C_Traits.GetNodeInfo}} or {{api|C_Traits.GetEntryInfo}}

==Returns==
:;condInfo:{{apitype|TraitCondInfo}} - returns nil if no info is found
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|condID}} || {{apitype|number}} || as supplied in the arguments
|-
| {{apiname|ranksGranted}} || {{apitype|number?}} || if the condition is met, this number of ranks is granted to applicable nodes
|-
| {{apiname|isAlwaysMet}} || {{apitype|boolean}} || generally false, no TraitConditions are currently used where this is true
|-
| {{apiname|isMet}} || {{apitype|boolean}} || True if the source for the condition has been fulfilled.
|-
| {{apiname|isGate}} || {{apitype|boolean}} || True if the condition is a Gate - this generally only impacts tooltips and class talent trees
|-
| {{apiname|isSufficient}} || {{apitype|boolean}} || <font color="green">11.0.2</font> - True if meeting the requirements for the condition means any nodes using this condition are considered fulfilled if the condition is met.
|-
| {{apiname|type}} || {{apitype|Enum.TraitConditionType}} || <font color="green">11.0.2</font> - The value from the TraitConditionType enum the condition uses.
|-
| {{apiname|questID}} || {{apitype|number?}} || no conditions seem to currently exist with this value - presumably these would require a quest to completed; or, less likely, require the quest to be in your questlog
|-
| {{apiname|achievementID}} || {{apitype|number?}} || condition is met if the achievement has been earned
|-
| {{apiname|specSetID}} || {{apitype|number?}} || condition is met if your spec matches any spec from the specified specSet (see {{api|C_SpecializationInfo.GetSpecIDs}})
|-
| {{apiname|playerLevel}} || {{apitype|number?}} || condition is met if you are at or above the specified level
|-
| {{apiname|traitCurrencyID}} || {{apitype|number?}} || combined with spentAmountRequired - matches the ID in [[Struct_TraitCurrencyCost|TraitCurrencyCost]] (see {{api|C_Traits.GetNodeCost}}, and {{api|C_Traits.GetTreeCurrencyInfo}})
|-
| {{apiname|spentAmountRequired}} || {{apitype|number?}} || condition is met if you spent the specified amount in the specified traitCurrency
|-
| {{apiname|tooltipFormat}} || {{apitype|string?}} || a tooltip string, potentially with placeholders suitable for string.format, which can be displayed if the condition isn't met
|-
| {{apiname|traitCondAccountElementID}} || {{apitype|number?}} || <font color="green">11.0.0</font>
|-
| <font color="pink">{{apiname|tooltipText}}</font> || {{apitype|string?}} || Blizzard_SharedTalentUI adds this data to the response manually, see [https://github.com/Gethe/wow-ui-source/blob/ptr/Interface/AddOns/Blizzard_SharedTalentUI/Blizzard_SharedTalentUtil.lua#L307-L342 Blizzard_SharedTalentUtil.lua]; the data is based on tooltipFormat, and adds quest/achievement/spec/level/spending info
|}

== Extra Info ==
Trait conditions have a specific types. Until 11.0.2 these types were not exposed in the API, the enum has always existed, and the information was available in the client DB files.
Conditions broadly fall into 2 categories, 'Friendly' and 'NotFriendly'. Friendly conditions give benefits if met, whereas NotFriendly conditions impose restrictions if not met.
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ style="text-align:left; margin-left: 2em" | Enum.TraitConditionType
! Value !! Field !! Category !! Description
|-
| 0 || {{apiname|Available}} || NotFriendly || Nodes are available by default, but if any condition of this type is '''not''' met, then the node is not available - e.g. Gates are implemented this way
|-
| 1 || {{apiname|Visible}} || NotFriendly || Nodes are visible by default, but if any condition of this type is '''not''' met, then the node is not visible - e.g. if a condition requires a specific spec, the node will be hidden
|-
| 2 || {{apiname|Granted}} || Friendly || Grants rank(s) for the relevant node
|-
| 3 || {{apiname|Increased}} || Friendly || No condition of this type currently exists, presumably they work similar to Granted
|-
| 4 || {{apiname|DisplayError}} || || <font color="green">11.0.2</font>
|}

{{apinavbox|C_Traits}}
```