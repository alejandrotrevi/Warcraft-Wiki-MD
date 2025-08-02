# API GetSpecializationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|future=1|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_DeprecatedSpecialization/Deprecated_Specialization_Standard.lua#L12-L13}}
Returns info for a specialization.
 id, name, description, icon, role, primaryStat = GetSpecializationInfo(specIndex [, isInspect, isPet, inspectTarget, sex])

==Arguments==
:;specIndex:{{apitype|number}} - Index of the specialization to query, ascending from 1 to {{api|GetNumSpecializations}}().
:;isInspect:{{apitype|boolean?}} - Whether to query specialization information for the inspected unit. ''Does not actually seem to work, you need to use {{api|GetInspectSpecialization}}() instead.''
:;isPet:{{apitype|boolean?}} - Whether to query specialization information for the player's pet.
:;inspectTarget:{{apitype|string?}} : [[UnitToken]] - The unit to request data for, when inspecting.
:;sex:{{apitype|number?}} - Player's sex as returned by {{api|UnitSex}}()

==Returns==
:;id:{{apitype|number}} : [[SpecializationID]]
:;name:{{apitype|string}} - Specialization name, e.g. "Balance".
:;description:{{apitype|string}} - Description of the specialization, e.g. "Can take on the form of a powerful Moonkin, balancing the power of Arcane and Nature magic to destroy enemies at a distance."
:;icon:{{apitype|number}} : [[FileID]]
:;role:{{apitype|string}} - The intended role in a party: <code>"DAMAGER", "TANK", "HEALER"</code>
:;primaryStat:{{apitype|number}} - The primary stat as listed in SPEC_STAT_STRINGS<ref>{{ref FrameXML|Blizzard_TalentUI/Blizzard_TalentUI.lua|6.0.2|19033|220|2014-10-14}}</ref>: <code>1=Strength, 2=Agility, 4=Intellect</code>

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|GetSpecialization}} }}
{{apirow | Related Events | {{api|t=e|PLAYER_SPECIALIZATION_CHANGED}} }}
|}

==Values==
:<span class="noexcerpt" data-nosnippet>''Linked from: [[SpecializationID]]''</span>
{{:SpecializationID}}

==Example==
<syntaxhighlight lang="lua">
GetSpecializationInfo(1)
> 256, "Discipline", "Uses magic to shield allies from taking damage as well as heal their wounds.\r\n\r\nPreferred Weapon: Staff, Wand, Dagger, Mace", 135940, "HEALER", 4
</syntaxhighlight>

==References==
```