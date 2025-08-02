# API KBSetup GetCategoryData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns information about a category.

 id, caption = KBSetup_GetCategoryData(index)

==Parameters==
===Arguments===
:(index)

:;index:{{apitype|number}} - Range from 1 to [[API_KBSetup_GetCategoryCount|KBSetup_GetCategoryCount]]()

===Returns===
:id, caption

:;id:{{apitype|number}} - The category's id.
:;caption:{{apitype|string}} - The category caption.

==Details==
* Seems to only work if KBSetup_IsLoaded() returns true.
```