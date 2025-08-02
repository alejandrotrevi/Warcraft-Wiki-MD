# API KBSetup GetArticleHeaderData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns header information about an article.

 id, title, isHot, isNew = KBSetup_GetArticleHeaderData(index)

==Parameters==
===Arguments===
:(index)

:;index:{{apitype|number}} - The articles index for that page.

===Returns===
:id, title, isHot, isNew

:;id:{{apitype|number}} - The article's id.
:;title:{{apitype|string}} - The article's title.
:;isHot:{{apitype|boolean}} - Show the "hot" symbol or not
:;isNew:{{apitype|boolean}} - Show the "new" symbol or not

==Example==
  local id, title, isHot, isNew = KBSetup_GetArticleHeaderData(1)
  if isNew then
    ChatFrame1:AddMessage("The article " .. id .. "(" .. title .. ") is new.", 1.0, 1.0, 1.0)
  end

==Details==
* This will work on the "most asked" articles, not the articles of the active query.
```