# API KBSetup GetSubCategoryCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns the number of subcategories in a category.

 count = KBSetup_GetSubCategoryCount(category)

==Parameters==
===Arguments===
:(category)

:;category:{{apitype|number}} - The category's index.

===Returns===
:count

:;count:{{apitype|number}} - Number of subcategories.

==Details==
* This is only available when KBSetup_IsLoaded() is true.
```