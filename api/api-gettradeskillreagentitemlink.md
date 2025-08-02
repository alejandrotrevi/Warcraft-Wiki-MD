# API GetTradeSkillReagentItemLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the link string for a trade skill reagent.
 link = GetTradeSkillReagentItemLink(skillId, reagentId)

==Arguments==
:;skillId:{{apitype|number}} - The Id specifying which trade skill's reagent to link.
:;reagentId:{{apitype|number}} - The Id specifying which of the skill's reagents to link.

==Returns==
:;link:{{apitype|string}} - An item link string (color coded with href) which can be included in chat messages to represent the reagent required for the trade skill.

==Details==
'''This function is broken on 5.2.0 build 16650 and always returns nil.'''
```