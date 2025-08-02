# API GetGuildBankMoneyTransaction

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a money transaction from the guild bank. <!-- PTR 0.3.0.7561 Blizzard_GuildBankUI.lua, line 555 -->
 transactionType, name, amount, years, months, days, hours = GetGuildBankMoneyTransaction(index)

==Arguments==
:;index:{{apitype|number}} - The index of the transaction to select. From 1 to [[API_GetNumGuildBankMoneyTransactions|GetNumGuildBankMoneyTransactions]]().

==Returns==
:;transactionType:{{apitype|string}} - The Type of transaction ("deposit" | "withdrawal" | "repair").
:;name:{{apitype|string}} - The User that performed a Transaction. A nil return indicates that this data is cached or possibly invalid! In the Blizzard UI nil users are said to be "Unknown"
:;amount:{{apitype|number}} - The Copper value of the Transaction.
:;years:{{apitype|number}} -  The number of years since this transaction took place.
:;months:{{apitype|number}} -  The number of months since this transaction took place.
:;days:{{apitype|number}} - The number of days since this transaction took place.
:;hours:{{apitype|number}} -  Hours Since the Transaction took place.

==Details==
WARNING:
This Lua function crashes the game client if the index is out of range. If QueryGuildBankLog(MAX_GUILDBANK_TABS+1) is not called and/or there is no player proximity to the guild bank this will return invalid (cached, lagged, or possibly random) data. When called incorrectly "repair" type transactions have been observed when the Blizzard UI does not show any repair transactions in that guild bank.
```