# API KBSetup IsLoaded

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Determine if the article list is loaded.

 loaded = KBSetup_IsLoaded()

==Parameters==
===Arguments===
:()

===Returns===
: loaded

:;loaded:{{apitype|boolean}} - True if the article list is loaded.

==Example==
  function KnowledgeBaseFrame_Search(resetCurrentPage)
    if ( not KBSetup_IsLoaded() ) then
      return;
    end
    -- ...
<small>''From Blizzard's KnowledgeBaseFrame.lua (l. 217 ff.)''</small>
```