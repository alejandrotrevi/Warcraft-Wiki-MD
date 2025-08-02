# API GetCurrentRegion

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a numeric ID representing the region the player is currently logged into.
 region = GetCurrentRegion()

==Returns==
:;region:{{apitype|number}} : {{dbc|Cfg_Regions|Cfg_Regions.Region_ID}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! ID !! Region || Description
|-
! colspan=3 | Retail
|-
| 1 || Retail US || includes Brazil and Oceania
|-
| 2 || Retail KR || 
|-
| 3 || Retail EU || includes Russia
|-
| 4 || Retail TW || See [[#Details]]
|-
| 5 || Retail CN || 
|-
| 50 || Retail PTR || 
|-
| 57 || Retail XPTR || 
|-
! colspan=3 | Arena
|-
| 21 || Arena US || 
|-
| 22 || Arena KR || 
|-
| 23 || Arena EU || 
|-
| 24 || Arena TW || 
|-
| 25 || Arena CN || 
|-
| 26 || Arena OC || 
|-
! colspan=3 | Classic Arena
|-
| 35 || Classic Arena US || 
|-
| 36 || Classic Arena KR || 
|-
| 37 || Classic Arena EU || 
|-
| 38 || Classic Arena TW || 
|-
| 39 || Classic Arena CN || 
|-
! colspan=3 | Classic
|-
| 40 || Classic PTR || 
|-
| 41 || Classic US || 
|-
| 42 || Classic KR || 
|-
| 43 || Classic EU || 
|-
| 44 || Classic TW || 
|-
| 45 || Classic CN || 
|-
! colspan=3 | Test
|-
| 60 || Dev 1 || 
|-
| 65 || Dev 2 || 
|-
| 70 || Classic Beta || 
|-
! colspan=3 | MDI
|-
| 71 || MDI US || 
|-
| 72 || MDI KR || 
|-
| 73 || MDI EU || 
|-
| 74 || MDI TW || 
|-
| 75 || MDI CN || 
|-
| 76 || MDI OC || 
|-
! colspan=3 | Classic Era
|-
| 80 || Classic Era PTR || 
|-
| 81 || Classic Era US || 
|-
| 82 || Classic Era KR || 
|-
| 83 || Classic Era EU || 
|-
| 84 || Classic Era TW || 
|-
| 85 || Classic Era CN || 
|}

==Details==
The value returned is deduced from the [[CVar portal|portal]] console variable, which may be set by the game client at launch to match the selected account region in the Battle.net desktop application. It does not necessarily indicate the region of the realm that the player is logged into, but instead the region of the Battle.net portal used to contact the login servers and provide a realm list.

This function is mostly reliable except in the case where the user modifies the portal from the login screen after having launched the game client through the Battle.net desktop application. The game client will prefer to use the login server addresses specified by the desktop application over the portal, causing a mismatch between the logged in region and what this function will report.

Realms located in Taiwan use the Korean Battle.net portal, meaning this function will typically always report the current region as being Korea rather than Taiwan when connected to these realms. Other functions like {{api|C_BattleNet.GetFriendAccountInfo}} may however return region IDs that correctly identify Taiwanese realms.

==Alternatives==

The following snippet demonstrates use of this API in conjunction with {{api|C_BattleNet.GetGameAccountInfoByGUID}} to more reliably obtain the current region ID of the player.

<syntaxhighlight lang="lua">
local function GetActualRegion()
    local gameAccountInfo = C_BattleNet.GetGameAccountInfoByGUID(UnitGUID("player"))
    return gameAccountInfo and gameAccountInfo.regionID or GetCurrentRegion()
end

print(GetActualRegion())
</syntaxhighlight>

==Patch changes==
* {{Patch 10.1.5|note=Test realms may no longer consistently return a value of 1 (US).}}
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|GetCurrentRegionName}}
```