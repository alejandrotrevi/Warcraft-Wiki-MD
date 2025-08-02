# API KBArticle GetData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns data for the current article.

 id, subject, subjectAlt, text, keywords, languageId, isHot = KBArticle_GetData()

==Parameters==
===Arguments===
:()

===Returns===
: id, subject, subjectAlt, text, keywords, languageId, isHot

:;id:{{apitype|number}} - The article id
:;subject:{{apitype|string}} - The localized title.
:;subjectAlt:{{apitype|string}} - The english title.
:;text:{{apitype|string}} - The article itself
:;keywords:{{apitype|string}} - Some keywords for the article. May be ''nil''.
:;languageId:{{apitype|number}} - The language ID for the article.
:;isHot:{{apitype|boolean}} - Flag for the "hot" status.


==Details==
* Only works if KBArticle_IsLoaded() returns true.
```