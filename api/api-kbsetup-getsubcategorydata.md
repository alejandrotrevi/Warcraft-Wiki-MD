# API KBSetup GetSubCategoryData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns information about a subcategory.

 id, caption = KBSetup_GetSubCategoryData(category, index)

==Parameters==
===Arguments===
:(category, index)

:;category:Intgeger - The category's index.
:;index:{{apitype|number}} - Range from 1 to [[API_KBSetup_GetSubCategoryCount|KBSetup_GetSubCategoryCount]](category)

===Returns===
:id, caption

:;id:{{apitype|number}} - The category's id.
:;caption:{{apitype|string}} - The category caption.

==Details==
* Only works if KBSetup_IsLoaded() returns true.
```