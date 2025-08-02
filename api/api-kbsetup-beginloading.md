# API KBSetup BeginLoading

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Starts the loading of articles.

 KBSetup_BeginLoading(articlesPerPage, currentPage)

==Parameters==
===Arguments===
:(articlesPerPage, currentPage)

:;articlesPerPage:{{apitype|number}} - Number of articles shown on one page.
:;currentPage:{{apitype|number}} - The current page (starts at 1).

===Returns===

:;nil

==Example==
In KnowledgeBaseFrame_OnShow():
  KBSetup_BeginLoading(KBASE_NUM_ARTICLES_PER_PAGE, KBASE_CURRENT_PAGE)
<small>''From Blizzard's KnowledgeBaseFrame.lua (l. 51)''</small>

==Details==
* This will start the article loading process and return immediately. 
* When all articles are loaded the event KNOWLEDGE_BASE_SETUP_LOAD_SUCCESS is fired.
* If an error occurs in the loading process, the event KNOWLEDGE_BASE_SETUP_LOAD_FAILURE is fired.
```