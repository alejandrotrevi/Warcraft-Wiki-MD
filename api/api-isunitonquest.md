# API IsUnitOnQuest

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the passed unit is on the passed quest. 
 IsUnitOnQuest(questIndex, unit) 

----
;''Arguments''
:;questIndex:{{apitype|number}} - The index of the quest to check for
:;unit:{{apitype|string}} : [[UnitId]]

----
;''Returns''

:;bool

----
;''Example''
    if IsUnitOnQuest(0, "player")  then
        SendChatMessage("i am on my quest", "SAY", "Common", "General")
    end

;''Result''
    <1. General>Player: "i am on my quest";
----
;''Description''

*Returns whether the specified unit is on the specified quest. One can use any of the defined [[API TYPE UnitId|UnitId]] values so long as it refers to a unit in the party or raid.
```