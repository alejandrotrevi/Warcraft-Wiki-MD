# API KBSetup GetLanguageData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns information about a language.

 id, caption = KBSetup_GetLanguageData(index)

==Parameters==
===Arguments===
:(index)

:;index:{{apitype|number}} - Range from 1 to [[API_KBSetup_GetLanguageCount|KBSetup_GetLanguageCount]]()

===Returns===
:id, caption

:;id:{{apitype|number}} - The internal language ID.
:;caption:{{apitype|string}} - The (localized?) name of the language.

==Details==
* Seems to only work if KBSetup_IsLoaded() returns true.
```