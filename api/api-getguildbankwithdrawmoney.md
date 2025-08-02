# API GetGuildBankWithdrawMoney

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the amount of money the player is allowed to withdraw from the guild bank.
 withdrawLimit = GetGuildBankWithdrawMoney()

==Returns==
:;withdrawLimit:{{apitype|number}} - Amount of money the player is allowed to withdraw from the guild bank (in copper), or 2^64 if the player has unlimited withdrawal privileges (is Guild Master)

==Details==
Returns the amount remaining for the day; that is (Daily amount) - (amount already spent).
```