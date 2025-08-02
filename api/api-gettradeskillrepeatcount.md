# API GetTradeskillRepeatCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of times the current item is being crafted.
 local repeatCount = GetTradeskillRepeatCount()

==Returns==
:;repeatCount:{{apitype|number}} - The number of times the current tradeskill item is being crafted.

==Details==
: The repeat count is initially set by the optional repeat parameter of [[API DoTradeSkill|DoTradeSkill]].
```