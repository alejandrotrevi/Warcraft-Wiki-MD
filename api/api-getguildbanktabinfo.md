# API GetGuildBankTabInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns info for a guild bank tab.
<!-- from PTR 0.3.0.7561 Blizzard_GuildBankUI.lua line 308 -->
 name, icon, isViewable, canDeposit, numWithdrawals, remainingWithdrawals, filtered = GetGuildBankTabInfo(tab)

==Arguments==
:("tab")

:;tab:{{apitype|number}} - The index of the guild bank tab. (result of GetCurrentGuildBankTab())
==Returns==
:name, icon, isViewable, canDeposit, numWithdrawals, remainingWithdrawals, filtered

:;name:{{apitype|string}} - Title of the bank tab.
:;icon:{{apitype|string}} - Path to the bank tab icon texture.
:;isViewable:{{apitype|boolean}} - True if the player can click on the bank tab.
:;canDeposit:{{apitype|boolean}} - True if the player can deposit items.
:;numWithdrawals:{{apitype|number}} - Available withdrawals per day.
:;remainingWithdrawals:{{apitype|number}} - Remaining withdrawals for the day.
:;filtered:{{apitype|boolean}} - True if the requested tab is filtered out.

==Details==

As of 4.0.3, the ''remainingWithdrawals'' value seems to be bugged, in that it returns the value for the currently selected tab rather than the tab passed to the function. This bug can be demonstrated by entering ''/dump GetGuildBankTabInfo(1)'' while viewing different tabs of the bank; the value returned reflects the currently viewed tab, rather than the first tab. You can get around this by calling [[API_QueryGuildBankTab|QueryGuildBankTab]](tabNum) before calling this function.
```