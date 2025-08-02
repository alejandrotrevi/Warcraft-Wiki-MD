# API GetSpecializationInfoByID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a specialization.
 id, name, description, icon, role, classFile, className = GetSpecializationInfoByID(specID)

==Arguments==
:;specID:{{apitype|number}} : [[SpecializationID]]

==Returns==
:;id:{{apitype|number}} : [[SpecializationID]]
:;name:{{apitype|string}} - Specialization name, e.g. "Balance".
:;description:{{apitype|string}} - Description of the specialization, e.g. "Can take on the form of a powerful Moonkin, balancing the power of Arcane and Nature magic to destroy enemies at a distance."
:;icon:{{apitype|number}} : [[FileID]]
:;role:{{apitype|string}} - The intended role in a party: <code>"DAMAGER", "TANK", "HEALER"</code>
:;classFile:{{apitype|string}} - Locale-independent class name, e.g. <code>"PRIEST"</code>
:;className:{{apitype|string}} - Localized class name, e.g. <code>"Priest"</code>

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
GetSpecializationInfoByID(256)
> 256, "Discipline", "Uses magic to shield allies from taking damage as well as heal their wounds.\r\n\r\nPreferred Weapon: Staff, Wand, Dagger, Mace", 135940, "HEALER", "PRIEST", "Priest"
</syntaxhighlight>
```