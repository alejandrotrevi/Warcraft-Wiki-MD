# API C Item.GetItemLocation

**Contributor:** Zeal

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Needs summary.
 itemLocation = C_Item.GetItemLocation(itemGUID)

==Arguments==
:;itemGUID:{{apitype|string}}

==Returns==
:;itemLocation:{{apitype|ItemLocationMixin?}}

==Notes==
*{{warning}} ''itemLocation''s returned for the ''itemGUID''s of bags in bank bag slots are invalid and cannot be used ([https://github.com/Stanzilla/WoWUIBugs/issues/537 Issue #537]).
```