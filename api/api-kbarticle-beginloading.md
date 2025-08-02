# API KBArticle BeginLoading

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Starts the article load process.

 KBArticle_BeginLoading(id, searchType)

==Parameters==
===Arguments===
:(id, searchType)

:;id:{{apitype|number}} - The article's ID
:;searchType:{{apitype|number}} - Search type for the loading process.

===Returns===

:;nil

==Details==
* The ''searchType'' can be either 1 or 2. 1 is used if the search text is empty, 2 otherwise.

==Example==
 function KnowledgeBaseArticleListItem_OnClick()
   local searchText = KnowledgeBaseFrameEditBox:GetText();
   local searchType = 2;
   if (searchText ==KBASE_DEFAULT_SEARCH_TEXT or searchText== "") then
     searchType = 1;
   end
   KBArticle_BeginLoading(this.articleId, searchType);
 end
<small>''From Blizzard's KnowledgeBaseFrame.lua (l. 529 ff.)''</small>
```