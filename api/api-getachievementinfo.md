# API GetAchievementInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an achievement.
 id, name, points, completed, month, day, year, description, flags,
 icon, rewardText, isGuild, wasEarnedByMe, earnedBy, isStatistic
     = GetAchievementInfo(achievementID)
     = GetAchievementInfo(categoryID, index)

==Arguments==
:;achievementID:{{apitype|number}} : ID of the achievement to retrieve information for.
----
:;categoryID:{{apitype|number}} - Achievement category ID.
:;index:{{apitype|number}} - An offset into the achievement category, between 1 and {{api|GetCategoryNumAchievements}}(categoryID)

==Returns==
{| class="darktable zebra col1-center"
! Index !! Param !! Type !! Description
|-
|1 || id || {{apitype|number}} || Achievement ID.
|-
|2 || name || {{apitype|string}} || The Name of the Achievement.
|-
|3 || points || {{apitype|number}} || Points awarded for completing this achievement.
|-
|4 || completed || {{apitype|boolean}} || Returns true/false depending if you've completed this achievement on any character.
|-
|5 || month || {{apitype|number}} || Month this was completed. Returns nil if Completed is false.
|-
|6 || day || {{apitype|number}} || Day this was completed. Returns nil if Completed is false.
|-
|7 || year || {{apitype|number}} || Year this was completed. Returns nil if Completed is false. Returns number of years since 2000.
|-
|8 || description || {{apitype|string}} || The Description of the Achievement.
|-valign="top"
|9 || flags || {{apitype|number}} || A bitfield that indicates achievement properties:
{{columns|minwidth=22em|
:0x1 - COUNTER
:0x2 - ?
:0x4 - PLAY_NO_VISUAL 
:0x8 - SUM
:0x10 - MAX_USED
:0x20 - REQ_COUNT
:0x40 - AVERAGE
:0x80 - PROGRESS_BAR
:0x100 - REALM_FIRST_REACH
:0x200 - REALM_FIRST_KILL
:0x400 - ?
:0x800 - HIDE_INCOMPLETE
:0x1000 - SHOW_IN_GUILD_NEWS
:0x2000 - SHOW_IN_GUILD_HEADER
:0x4000 - GUILD
:0x8000 - SHOW_GUILD_MEMBERS
:0x10000 - SHOW_CRITERIA_MEMBERS
:0x20000 - ACCOUNT_WIDE
:0x40000 - UNK5
:0x80000 - HIDE_ZERO_COUNTER
:0x100000 - TRACKING_FLAG
:0x200000 - ?
:0x400000 - ?
:0x800000 - ?
}}
|-
|10 || icon || {{apitype|number}} || The [[fileID]] of the icon used for this achievement
|-
|11 || rewardText || {{apitype|string}} || Text describing the reward you get for completing this achievement.
|-
|12 || isGuild || {{apitype|boolean}} || Returns true/false depending if this is a guild achievement.
|-
|13 || wasEarnedByMe || {{apitype|boolean}} || Returns true/false depending if you've completed this achievement on this character.
|-
|14 || earnedBy || {{apitype|string}} || Your character name if you've completed this achievement, or the name of the first character to complete this achievement.
|-
|15 || isStatistic || {{apitype|bool}} || Returns true/false depending if this is a statistic.
|}

==Patch changes==
* {{Patch 7.3.0|note=Tenth return value (the icon) changed from a string texture path to a [[fileID]].}}
* {{Patch 3.0.2|note=Added.}}

==See also==
* {{api|GetCategoryList}}
* {{api|GetCategoryNumAchievements}}
<!-- luals
---@param achievementID number
---@return number id
---@return string name
---@return number points
---@return boolean completed
---@return number month
---@return number day
---@return number year
---@return string description
---@return number flags
---@return number icon
---@return string rewardText
---@return boolean isGuild
---@return boolean wasEarnedByMe
---@return string earnedBy
---@return boolean isStatistic
---@overload fun(categoryID: number, index: number)
function GetAchievementInfo(achievementID) end
-->
```