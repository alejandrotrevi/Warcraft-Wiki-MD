# API C UnitAuras.AddPrivateAuraAppliedSound

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UnitAuras|system=UnitAuras}}
Needs summary.
 privateAuraSoundID = C_UnitAuras.AddPrivateAuraAppliedSound(sound)

==Arguments==
:;sound:{{apitype|UnitPrivateAuraAppliedSoundInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| unitToken || {{apitype|string}} || 
|-
| spellID || {{apitype|number}} || 
|-
| soundFileName || {{apitype|string?}} || 
|-
| soundFileID || {{apitype|number?}} || 
|-
| outputChannel || {{apitype|string?}} || 
|}

==Returns==
:;privateAuraSoundID:{{apitype|number?}}
```