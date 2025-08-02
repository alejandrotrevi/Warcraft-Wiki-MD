# API SetCurrentTitle

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Sets the player's displayed title.
 SetCurrentTitle(titleId)

==Arguments==
:;titleId:{{apitype|number}} : [[TitleId]] - ID of the title you want to set. The identifiers are global and therefore do not depend on which titles you have learned. <code>0</code>, invalid or unlearned IDs clear your title.

==Details==
* The last indexed value (currently 143) returns nil and removes the player's name completely (not available to players).
* [[API GetTitleName|GetTitleName]] can be used to find the name associated with the [[TitleId]].

==Example==
This sets the title "Elder" if your character had earned the title, otherwise it removes any active title.
 SetCurrentTitle(43)

Sets a random title from the available ones.
<syntaxhighlight lang="lua">
/run local t = {} for i = 1, GetNumTitles() do if IsTitleKnown(i) then tinsert(t, i) end end SetCurrentTitle(t[random(#t)])
</syntaxhighlight>
```