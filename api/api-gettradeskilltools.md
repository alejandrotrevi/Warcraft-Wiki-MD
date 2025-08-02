# API GetTradeSkillTools

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the required tools for a specific trade skill.
 GetTradeSkillTools(skillIndex)

----
;''Arguments''

: none

----
;''Returns''

: ListString tools

:;tools:The tools required for the tradeskill

----
;''Example''

Prints the tools required for the tradeskill to the chatwindow.
 ChatFrame1:AddMessage(BuildColoredListString(GetTradeSkillTools(skillIndex)));
```