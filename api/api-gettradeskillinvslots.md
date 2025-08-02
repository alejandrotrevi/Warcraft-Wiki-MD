# API GetTradeSkillInvSlots

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of the available inventory slot types
 invSlots = GetTradeSkillInvSlots()

----
;''Arguments''

: none

----
;''Returns''

:;invSlots:ListString : The available inventory slot types

----
;''Example''

Prints the available inventory slot types to the chatwindow
 ChatFrame1:AddMessage(GetTradeSkillInvSlots());

----
;''Example''

Gets available inventory slots as a table of strings
 local t = {GetTradeSkillInvSlots()};
```