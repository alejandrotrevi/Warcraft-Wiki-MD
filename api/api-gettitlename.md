# API GetTitleName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of a player title.
 name, playerTitle = GetTitleName(titleId)

==Arguments==
:;[[TitleId|titleId]]:{{apitype|number}} - Ranging from 1 to {{api|GetNumTitles}}. Not necessarily an index as there can be missing/skipped IDs in between.

==Returns==
:;name:{{apitype|string}} - Name of the title.
:;playerTitle:{{apitype|boolean}} - Seems to be true for all existing titles.

==Details==
* If the name has a trailing space, then the title is prefixed, otherwise it's suffixed.
<syntaxhighlight lang="lua">
/dump GetTitleName(2) -- "Corporal " → "Corporal Bob" (prefix)
/dump GetTitleName(36) -- "Champion of the Naaru" → "Alice, Champion of the Naaru" (suffix)
</syntaxhighlight>

==Patch changes==
* {{Patch 2.0.1|note=Added.}}

==See also==
* {{api|GetCurrentTitle}}
* {{api|IsTitleKnown}}
```