# API ExpandTradeSkillSubClass

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Expands a header within a tradeskill window.
 ExpandTradeSkillSubClass(index)

==Arguments==
:;index:{{apitype|number}} - index within the tradeskill window

==Triggers events==
It is unknown whether an event triggers.

==Example==
 _, skillType, _, isExpanded, _, _ = [[API GetTradeSkillInfo|GetTradeSkillInfo]](skillIndex)
 for index = GetNumTradeSkills(), 1, -1 do
     if skillType == "header" then
         ExpandTradeSkillSubClass(index)
     end
 end

<big>'''Result'''</big>
All your currently-listed subclasses will be expanded. Subclasses that are folded within another will remain at their former state, collapsed or expanded.

==Details==
: No error is generated when already isExpanded.
: An error is generated when the skillType ~= "header": ''Bad skill line in ExpandTradeSkillSubClass''
```