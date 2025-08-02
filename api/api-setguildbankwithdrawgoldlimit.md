# API SetGuildBankWithdrawGoldLimit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the gold withdraw limit for the guild bank.
 SetGuildBankWithdrawGoldLimit(amount)

==Arguments==
:;amount:{{apitype|number}} - the amount of gold to withdraw per day

==Details==
: Sets the value of the Gold Withdrawal field for the current rank (used for repairs and direct withdrawls).  These changes are not saved until a call to [[API GuildControlSaveRank|GuildControlSaveRank]]() is made.  In order to actually withdraw or use guild repairs, the flags for those actions must be set using [[API GuildControlSetRankFlag|GuildControlSetRankFlag]]().
```