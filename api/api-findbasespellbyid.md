# API FindBaseSpellByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the ID for the base spell.
 baseSpellID = FindBaseSpellByID(spellID)

==Arguments==
:;spellID:{{apitype|number}} - The override spell ID

==Returns==
:;baseSpellID:{{apitype|number}}

==Details==
* Base spells are those overridden by another spell; override spells are usually gained via talents.
** For example, [[Backstab]] is the base spell for [[Gloomblade]].
** Another example, Rogue [[Stealth]] can be overridden with another version of stealth that is enhanced with the [[Shadowrunner]] talent.
* If querying with a spellID that does not actively override a base spell, then its own spellID will be returned.
** For example, querying with [[Backstab]] will return Backstab.
** Likewise, querying with [[Gloomblade]] when the talent is unknown will return Gloomblade.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|FindSpellOverrideByID}}
```