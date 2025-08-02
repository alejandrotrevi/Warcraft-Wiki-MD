# API C Spell.GetSpellInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns spell info.
 spellInfo = C_Spell.GetSpellInfo(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}} - Using name will always check for an override on that spell; If passed a spell ID, will return same id as was passed.

==Returns==
:;spellInfo:{{apitype|SpellInfo?}} - Returns nil if spell is not found
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|name}} || {{apitype|string}} || The localized name of the spell
|-
| {{apiname|iconID}} || {{apitype|fileID}} || Icon for this spell; If spell has been overriden, this may be the icon for the overriding spell; See <code>originalIconID</code> for the nonoverridden icon
|-
| {{apiname|originalIconID}} || {{apitype|fileID}} || <font color="green">11.0.0</font> - The original icon texture for this spell
|-
| {{apiname|castTime}} || {{apitype|number}} || Cast time in milliseconds, or 0 for instant spells
|-
| {{apiname|minRange}} || {{apitype|number}} || Minimum range of the spell, or 0 if not applicable
|-
| {{apiname|maxRange}} || {{apitype|number}} || Maximum range of the spell, or 0 if not applicable
|-
| {{apiname|spellID}} || {{apitype|number}} || The ID of the spell
|}

==Details==
* If only a single spell field is needed, try using one of the new more specific getters in [[:Category:API_namespaces/C_Spell|C_Spell]] instead of a full Get Info: {{api|C_Spell.GetSpellName}}, {{api|C_Spell.GetSpellTexture}}, etc.
* The player's form or stance may affect return values on relevant spells, such as a warlock's Corruption spell transforming to Doom while Metamorphosis is active.
* When dealing with base spells that have been overridden by another spell, the <code>icon</code> return will represent the icon of the overriding spell, and <code>originalIcon</code> the icon of the base spell.
** For example, if a Rogue has learned [[Gloomblade]] then any queries for [[Backstab]] will yield Gloomblades' icon as the <code>icon</code> return, and the original icon for Backstab would be exposed through the <code>originalIcon</code> return value.

==Example==
<syntaxhighlight lang="lua">
/dump C_Spell.GetSpellInfo(2061) -- [1]={castTime=1317, name="Flash Heal", minRange=0, originalIconID=135907, iconID=135907, maxRange=40, spellID=2061}
</syntaxhighlight>

===Asynchronous Querying===
{{:SpellMixin}}

==Patch changes==
* {{Patch 11.0.0|note=Added; returns a structured table. Replacement for {{api|GetSpellInfo}} and {{api|C_SpellBook.GetSpellInfo}}.}}
```