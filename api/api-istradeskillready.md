# API IsTradeSkillReady

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the list of trade skill abilities for the currently open trade skill is available.
 ready = IsTradeSkillReady()

==Returns==
:;ready:{{apitype|boolean}} - true if trade skill information is available, false if it is still being retrieved.

==Details==
* Trade skill information (the list of items the player is able to craft) for the player's character is streamed to the client when the character logs in.
* If you open a trade skill window before this process completes, this function will return <code>false</code>. {{api|t=e|TRADE_SKILL_UPDATE}} will fire again once information is available.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}
```