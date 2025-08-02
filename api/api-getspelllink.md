# API GetSpellLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the hyperlink for a spell.
 link, spellId = GetSpellLink(spell]
               = GetSpellLink(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;link:{{apitype|string}} : [[Hyperlinks#spell|spellLink]]
:;spellID:{{apitype|number}}

==Example==
Prints a clickable spell link, for [https://www.wowhead.com/spell=2061/flash-heal Flash Heal].
<syntaxhighlight lang="lua">
/run print(GetSpellLink(2061))
</syntaxhighlight>

Dumps an (escaped) spell link.
<syntaxhighlight lang="lua">
/dump GetSpellLink(2061)
-- "|cff71d5ff|Hspell:2061:0|h[Flash Heal]|h|r", 2061
</syntaxhighlight>

Dumps the first spell from your spell book.
<syntaxhighlight lang="lua">
/dump GetSpellLink(1, BOOKTYPE_SPELL)
-- "|cff71d5ff|Hspell:6603:0|h[Auto Attack]|h|r", 6603
</syntaxhighlight>

==Patch changes==
* {{Patch 2.4.0|note=Added.}}
```