# API GetGuildBankTransaction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns info for an item transaction from the guild bank.
 type, name, itemLink, count, tab1, tab2, year, month, day, hour = GetGuildBankTransaction(tab, index)

==Arguments==
:;tab:{{apitype|number}} - Tab number, ascending from 1 to [[API GetNumGuildBankTabs|GetNumGuildBankTabs]]().
:;index:{{apitype|number}} - Transaction index, ascending from 1 to [[API GetNumGuildBankTransactions|GetNumGuildBankTransactions]](tab). Higher indices correspond to more recent entries.

==Returns==
:;type:{{apitype|string}} - Transaction type. ("deposit", "withdraw" or "move")
:;name:{{apitype|string}} - Name of player who made the transaction.
:;itemLink:{{apitype|string}} - [[itemLink]] of transaction item.
:;count:{{apitype|number}} - Amount of items.
:;tab1:{{apitype|number}} - For type=="move", this is the origin tab.
:;tab2:{{apitype|number}} - For type=="move", this is the destination tab.
:;year:{{apitype|number}} - The number of years since this transaction took place.
:;month:{{apitype|number}} - The number of months since this transaction took place.
:;day:{{apitype|number}} - The number of days since this transaction took place.
:;hour:{{apitype|number}} - The number of hours since this transaction took place.
```