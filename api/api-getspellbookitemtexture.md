# API GetSpellBookItemTexture

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the icon texture of a spellbook item.
 icon = GetSpellBookItemTexture(spell)
      = GetSpellBookItemTexture(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;icon:{{apitype|number}} : [[FileID]] - Icon fileId for the queried entry, or nil if the queried item does not exist.

==Patch changes==
* {{Patch 7.0.3|note=The icon is now returned as a [[fileID]] rather than a texture path.}}
* {{Patch 4.0.1|note=Added.}}

==See also==
* {{api|GetSpellBookItemInfo}}
* {{api|GetSpellBookItemName}}
```