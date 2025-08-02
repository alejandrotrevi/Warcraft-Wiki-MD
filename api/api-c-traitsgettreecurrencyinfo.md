# API C Traits.GetTreeCurrencyInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Returns the list of TraitCurrencies related to a TraitTree.
 treeCurrencyInfo = C_Traits.GetTreeCurrencyInfo(configID, treeID, excludeStagedChanges)

==Arguments==
:;configID:{{apitype|number}} - For TalentTrees this will often be {{api|C_ClassTalents.GetActiveConfigID}}, this is -1 when inspecting a player. For professions, this will be {{api|C_ProfSpecs.GetConfigIDForSkillLine}}.
:;treeID:{{apitype|number}} - For TalentTrees a class specific TreeID, for professions {{api|C_ProfSpecs.GetSpecTabIDsForSkillLine}}.
:;excludeStagedChanges:{{apitype|boolean}} - If true, the committed value is returned; if false, the staged value is returned instead.

==Returns==
:;treeCurrencyInfo:{{apitype|TreeCurrencyInfo[]}} - For TalentTrees, the first currency returned is for the class points, the second currency is spec points.
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| traitCurrencyID || {{apitype|number}} || Can be used in e.g. {{api|C_Traits.GetNodeCost}} and {{api|C_Traits.GetTraitCurrencyInfo}}
|-
| quantity || {{apitype|number}} || How much currency is available to be used, e.g. available talent points, or profession knowledge.
|-
| maxQuantity || {{apitype|number?}} || For TalentsTrees, the amount of points available at your current level.
|-
| spent || {{apitype|number}} || The amount of currency already spent on traits.
|}

{{apinavbox|C_Traits}}
```