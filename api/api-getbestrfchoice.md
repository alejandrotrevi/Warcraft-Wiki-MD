# API GetBestRFChoice

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the suggested raid for the Raid Finder.
 dungeonId = GetBestRFChoice()

==Returns==
:;dungeonId:{{apitype|number}} : [[LfgDungeonID]]

==Example==
<syntaxhighlight lang="lua">
/dump GetBestRFChoice()
-- 416
</syntaxhighlight>

==See also==
* {{api|GetRFDungeonInfo}}
```