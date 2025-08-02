# API C Garrison.GetFollowerInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a follower.
 info = C_Garrison.GetFollowerInfo(followerID)

==Arguments==
:;followerID:{{apitype|number,string}} - a [[GarrFollowerID|FollowerID]] e.g. <code>856</code>
:::::: or a [[GUID#Follower|FollowerGUID]] e.g. <code>"0x0000000004CBDB61"</code>. Only works for the followers belonging to a character while on that character.

==Returns==
:;info:{{apitype|GarrFollowerInfo}} - Certain information is only returned when using a GUID from an existing follower.
{{:Struct_GarrFollowerInfo|nocaption=1}}

==Details==
quirk: If an ID is passed instead of a GUID, then <code>followerID</code> will be that ID instead, and <code>garrFollowerID</code> will be <code>nil</code>.
<syntaxhighlight lang="lua">
local a = C_Garrison.GetFollowers()[1]
print(a.followerID, a.garrFollowerID)           -- "0x0000000004CBDB61", 856

local byGUID = C_Garrison.GetFollowerInfo(a.followerID)
local byID = C_Garrison.GetFollowerInfo(a.garrFollowerID)
print(byGUID.followerID, byGUID.garrFollowerID) -- "0x0000000004CBDB61", 856
print(byID.followerID, byID.garrFollowerID)     -- 856, nil
</syntaxhighlight>

==Example==
* Dumps a follower by ID.
<syntaxhighlight lang="lua">
local follower = C_Garrison.GetFollowerInfo(856)
DevTools_Dump(follower)
</syntaxhighlight>
<syntaxhighlight lang="lua">
{
	classAtlas = "GarrMission_ClassIcon-Priest-Discipline",
	className = "Discipline Priest",
	classSpec = 124
	displayHeight = 0.5,
	displayIDs = {
		[1] = {
			id = 67797,
			followerPageScale = 1
		}
	},
	displayScale = 1,
	followerID = 856,
	followerTypeID = 4,
	height = 1,
	iLevel = 760,
	isFavorite = false,
	isMaxLevel = false,
	level = 35,
	name = "Calia Menethil",
	portraitIconID = 1401872,
	quality = 1,
	scale = 0.69999998807907,
}
</syntaxhighlight>


* Dumps the first follower by GUID. Although {{api|C_Garrison.GetFollowers}}() already returns the same data.
<syntaxhighlight lang="lua">
local followers = C_Garrison.GetFollowers()
local guid = followers[1].followerID
--local id = followers[1].garrFollowerID
DevTools_Dump(C_Garrison.GetFollowerInfo(guid))
</syntaxhighlight>
<syntaxhighlight lang="lua">
{
	classAtlas = "GarrMission_ClassIcon-Priest-Discipline",
	className = "Discipline Priest",
	classSpec = 124,
	displayHeight = 0.5,
	displayIDs = {
		[1] = {
			followerPageScale = 1,
			showWeapon = true,
			id = 67797
		}
	},
	displayScale = 1,
	followerID = "0x0000000004CBDB61",
	followerTypeID = 4,
	garrFollowerID = 856
	height = 1,
	iLevel = 900,
	isAutoTroop = false,
	isCollected = true,
	isFavorite = false,
	isMaxLevel = true,
	isSoulbind = false,
	isTroop = false,
	level = 45,
	levelXP = 200000,
	name = "Calia Menethil",
	portraitIconID = 1401872,
	quality = 4,
	scale = 0.69999998807907,
	slotSoundKitID = 62813,
	xp = 60600,
}
</syntaxhighlight>

==Patch changes==
* {{Patch 6.0.2|note=Added.}}

<!-- luals
---@param followerID number|string
---@return GarrFollowerInfo info
function C_Garrison.GetFollowerInfo(followerID) end

---@class GarrFollowerInfo
---@field classAtlas string
---@field className string
---@field classSpec number
---@field displayHeight number
---@field displayIDs DisplayInfo[]
---@field displayScale number
---@field followerID string|number
---@field followerTypeID number
---@field garrFollowerID? number
---@field height number
---@field iLevel number
---@field isAutoTroop? boolean
---@field isCollected? boolean
---@field isFavorite boolean
---@field isMaxLevel boolean
---@field isSoulbind? boolean
---@field isTroop? boolean
---@field level number
---@field levelXP? number
---@field name string
---@field portraitIconID number
---@field quality Enum.ItemQuality
---@field scale number
---@field slotSoundKitID? number
---@field status? string
---@field xp? number

---@class DisplayInfo
---@field followerPageScale number
---@field id number
---@field showWeapon? boolean
-->
```