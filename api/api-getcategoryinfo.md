# API GetCategoryInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an achievement category.

 title, parentCategoryID, flags = GetCategoryInfo(categoryID)

----
==Arguments==
:(Number categoryID)

:;categoryID:{{apitype|number}}


==Returns==
:;title:{{apitype|string}} - Title of the category.
:;parentCategoryID:{{apitype|number}} - id of the parent category or -1 if the category has no parent.
:;flags:{{apitype|number}} (bitfield)

==Patch changes==
* {{Patch 3.0.2|note=Added.}}

==See also==
*{{api|GetStatistic}}
*{{api|GetStatisticsCategoryList}}
*{{api|GetCategoryList}}
```