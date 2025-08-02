# API GetSpecializationInfoForClassID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a specialization.
 id, name, description, icon, role, recommended, allowedForBoost, masterySpell1, masterySpell2
   = GetSpecializationInfoForClassID(classID, index [, gender])
   = GetSpecializationInfoForSpecID(specID [, gender])

==Arguments==
===<font color="#4ec9b0">GetSpecializationInfoForClassID</font>===
:;classID:{{apitype|number}} : [[ClassId]]
:;index:{{apitype|luaIndex}}
:;gender:{{apitype|Enum.UnitSex?}}

===<font color="#4ec9b0">GetSpecializationInfoForSpecID</font>===
:;specID:{{apitype|number}} : [[SpecializationID]]
:;gender:{{apitype|Enum.UnitSex?}}
{{:Enum.UnitSex|nocaption=1}}

==Returns==
:;id:{{apitype|number}}: [[SpecializationID]]
:;name:{{apitype|string}} - Specialization name, e.g. "Balance".
:;description:{{apitype|string}} - Description of the specialization, e.g. "Can take on the form of a powerful Moonkin, balancing the power of Arcane and Nature magic to destroy enemies at a distance."
:;icon:{{apitype|fileID}}
:;role:{{apitype|string}} - The intended role in a party: <code>"DAMAGER", "TANK", "HEALER"</code>
:;recommended:{{apitype|boolean}} - If this specialization is recommended for beginners to the class.
:;allowedForBoost:{{apitype|boolean}} - If the player is allowed to use this specialization.
:;masterySpell1:{{apitype|number?}}
:;masterySpell2:{{apitype|number?}}

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
GetSpecializationInfoForClassID(5, 1)
> 256, "Discipline", "Uses magic to shield allies from taking damage as well as heal their wounds.\r\n\r\nPreferred Weapon: Staff, Wand, Dagger, Mace", 135940, "HEALER", true, false

GetSpecializationInfoForSpecID(256)
> 256, "Discipline", "Uses magic to shield allies from taking damage as well as heal their wounds.\r\n\r\nPreferred Weapon: Staff, Wand, Dagger, Mace", 135940, "HEALER", true, false
</syntaxhighlight>
```