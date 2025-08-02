# API GetGuildBankMoney

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the amount of money in the guild bank.
 retVal1 = GetGuildBankMoney()

==Returns==
:;retVal1:{{apitype|number}} - money in copper

==Example==
 /script DEFAULT_CHAT_FRAME:AddMessage(GetGuildBankMoney());

<big>'''Result'''</big>
 8900000

==Details==
Will return 0 (zero) if the guild bank frame was not opened, or a cached value from the last time the guild bank frame was opened on any character since the game client was started.
```