# API GetSocketItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the item currently being socketed.
 name, icon, quality = GetSocketItemInfo()

==Returns==
:;name:{{apitype|string}} - Localized name of the item currently being socketed, or nil if the socketing UI is not open.
:;icon:{{apitype|fileID}}
:;quality:{{apitype|Enum.ItemQuality}}
```