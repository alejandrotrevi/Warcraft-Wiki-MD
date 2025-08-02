# API GetSpellInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns spell info.
 name, rank, icon, castTime, minRange, maxRange, spellID, originalIcon
     = GetSpellInfo(spell)
     = GetSpellInfo(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;name:{{apitype|string}} - The localized name of the spell.
:;rank:{{apitype|string}} - Always returns <code>nil</code>. Refer to {{api|GetSpellSubtext}}() for retrieving the rank of spells on Classic.
:;icon:{{apitype|number}} : [[FileID]] - The spell icon texture.
:;castTime:{{apitype|number}} - Cast time in milliseconds, or 0 for instant spells.
:;minRange:{{apitype|number}} - Minimum range of the spell, or 0 if not applicable.
:;maxRange:{{apitype|number}} - Maximum range of the spell, or 0 if not applicable.
:;spellID:{{apitype|number}} - The ID of the spell.
:;originalIcon:{{apitype|number}} : [[FileID]] - The original icon texture for this spell.

==Details==
* The player's form or stance may affect return values on relevant spells, such as a warlock's Corruption spell transforming to Doom while Metamorphosis is active.
* When dealing with base spells that have been overridden by another spell, the <code>icon</code> return will represent the icon of the overriding spell, and <code>originalIcon</code> the icon of the base spell.
** For example, if a Rogue has learned [[Gloomblade]] then any queries for [[Backstab]] will yield Gloomblades' icon as the <code>icon</code> return, and the original icon for Backstab would be exposed through the <code>originalIcon</code> return value.

==Example==
<syntaxhighlight lang="lua">
/dump GetSpellInfo(2061) -- "Flash Heal", nil, 135907, 1352, 0, 40, 2061
</syntaxhighlight>

{{:SpellMixin}}

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_Spell.GetSpellInfo}} and returns a structured table.}}
* {{Patch 10.0.0|note=Added <code>originalIcon</code> return value.}}
* {{Patch 8.0.1|note=The <code>rank</code> return value is now always <code>nil</code>.<ref>[https://us.battle.net/forums/en/wow/topic/20762318007 ''Battle for Azeroth Addon Changes''] by [[Ythisens]], 24 Apr 2018</ref>}}
* {{Patch 6.0.2|note=Removed <code>cost, isFunnel, powerType</code> return values.}}

==References==
```