# API GetGuildBankWithdrawGoldLimit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns withdraw limit for currently selected rank in guild control.
 dailyWithdrawLimit = GetGuildBankWithdrawGoldLimit()

==Returns==
:;dailyWithdrawLimit:{{apitype|number}} - amount (in GOLD) the currently selected Guild Rank can withdraw per day

==Details==
In order for this to work properly, you need to have a rank set in the guildControl

==Example==
Checking the daily limit for the currently logged on character
<syntaxhighlight lang="lua">
-- create somewhere to store the result and default it
local dailyGoldWithdrawlLimit = 0

-- need to get the guildRankIndex for the currently logged on player
guildName, _, guildRankIndex = GetGuildInfo("player")
-- guildName is nil if the character isn't in a guild
if (guildName ~= nil) then
    -- This character is in a guild, so set the current rank so the limit will work
    GuildControlSetRank(guildRankIndex)
    dailyGoldWithdrawlLimit = GetGuildBankWithdrawGoldLimit()
end
</syntaxhighlight>

NOTE: this return value is in GOLD unlike many other currency returns in WOW where they give you copper pieces...
```