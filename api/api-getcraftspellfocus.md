# API GetCraftSpellFocus

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
 catalystName, number1 = GetCraftSpellFocus(index)

===Arguments===
:;index:{{apitype|number}} - 1 to [[API GetNumCrafts|GetNumCrafts()]]

===Returns===
When called while the enchanting screen is open, this function returns which rod is required, if any. I don't know whether this function also applies to other types of crafts or spells.

Returns two values when a rod is required: a string that contains the name of the rod, and the number "1". I don't know what the "1" means.

Returns nil if no rods are required.

==Patch changes==
* {{Patch 3.0.2|note=Removed.}}
```