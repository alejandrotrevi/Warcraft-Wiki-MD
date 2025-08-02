# API KBSetup GetTotalArticleCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}__NOTOC__
Returns the number of articles.

 count = KBSetup_GetTotalArticleCount()

==Parameters==
===Arguments===
:()

===Returns===
:count

:;count:{{apitype|number}} - The number of articles.

==Example==
  local count = KBSetup_GetTotalArticleCount()
  for i=1, count do
    -- do something with the article

==Details==
* This will count the "most asked" articles, not the number of articles for the active query.
```