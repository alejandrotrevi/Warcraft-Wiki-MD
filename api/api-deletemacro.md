# API DeleteMacro

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0.1}}
Deletes a macro.
 DeleteMacro(indexOrName)

==Arguments==
The sole argument has two forms to identify which macro to delete.
:;indexOrName:{{apitype|number,string}} - Index ranging from 1 to 120 for account-wide macros and 121 to 138 for character-specific ones or name of the macro to delete.

==Example==
Deleting all global macros:<syntaxhighlight lang="lua">
-- Start at the end, and move backward to first position (1).
for i = 0 + select(1,GetNumMacros()), 1, -1 do
	DeleteMacro(i)
end
</syntaxhighlight>Deleting all character-specific macros:
<syntaxhighlight lang="lua">
-- Start at the end, and move backward to first position (121).
for i = 120 + select(2,GetNumMacros()), 121, -1 do
	DeleteMacro(i)
end
</syntaxhighlight>

==Patch changes==
* {{Patch 2.0.1|note=Protected during combat,<ref name="2.0.1-Iriel">{{ref web|author=[[Iriel]]|archiveurl=http://blue.cardplace.com/newcache/us/36975623.htm|date=2006-10-23|title=2.0 Changes - Concise List (New)|url=http://forums.worldofwarcraft.com/thread.html?topicId=36975623&pageNo=1&sid=1#0}}</ref> but now also accepts a macro's name as an argument.<ref name="2.0.1-slouken">{{ref web|author={{Blizz}}[[slouken]]|archiveurl=http://blue.cardplace.com/newcache/us/15401595.htm|date=2006-10-19|title=Re: Expansion Changes - Concise List|url=http://forums.worldofwarcraft.com/thread.html?topicId=15401595&pageNo=41&sid=1#815}}</ref>}}

==See also==
* {{api|GetMacroInfo()}}
* {{api|EditMacro()}}
* {{api|PickupMacro()}}

==References==
{{Reflist}}
```