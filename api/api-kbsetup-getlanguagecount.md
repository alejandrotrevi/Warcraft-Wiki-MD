# API KBSetup GetLanguageCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns the number of languages in the knowledge base.

 count = KBSetup_GetLanguageCount()

==Parameters==
===Arguments===
:()

===Returns===
: count

:;count:Integert - The number of the available languages.

==Details==
* Seems to only work if KBSetup_IsLoaded() returns true.
* On a EU client this function returns ''4'' (enUS, deDE, frFR, esES).
```