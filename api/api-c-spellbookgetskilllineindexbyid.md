# API C SpellBook.GetSkillLineIndexByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Needs summary.
 skillIndex = C_SpellBook.GetSkillLineIndexByID(skillLineID)

==Arguments==
:;skillLineID:{{apitype|number}}

==Returns==
:;skillIndex:{{apitype|number?}} - Will be nil if the specified SkillLine could not be found, or if it is not one of the player's tracked skill lines

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```