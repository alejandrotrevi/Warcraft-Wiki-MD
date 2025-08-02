# API C Traits.GetDefinitionInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Needs summary.
 definitionInfo = C_Traits.GetDefinitionInfo(definitionID)

==Arguments==
:;definitionID:{{apitype|number}}

==Returns==
:;definitionInfo:{{apitype|TraitDefinitionInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| spellID || {{apitype|number?}} || 
|-
| overrideName || {{apitype|string?}} || 
|-
| overrideSubtext || {{apitype|string?}} || 
|-
| overrideDescription || {{apitype|string?}} || 
|-
| overrideIcon || {{apitype|number?}} || 
|-
| overriddenSpellID || {{apitype|number?}} || 
|-
| subType || {{apitype|Enum.TraitDefinitionSubType?}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.TraitDefinitionSubType
! Value !! Field !! Description
|-
| 0 || DragonflightRed || 
|-
| 1 || DragonflightBlue || 
|-
| 2 || DragonflightGreen || 
|-
| 3 || DragonflightBronze || 
|-
| 4 || DragonflightBlack || 
|}

{{apinavbox|C_Traits}}
```