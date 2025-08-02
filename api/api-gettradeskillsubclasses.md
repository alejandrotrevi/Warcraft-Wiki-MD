# API GetTradeSkillSubClasses

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of the valid subclasses.
 subClasses = GetTradeSkillSubClasses()

----
;''Arguments''

: none

----
;''Returns''

:;subClasses:ListString : The valid subclasses

----
;''Example''

Prints the valid subclasses to the chatwindow
 ChatFrame1:AddMessage(BuildListString(GetTradeSkillSubClasses()));
```