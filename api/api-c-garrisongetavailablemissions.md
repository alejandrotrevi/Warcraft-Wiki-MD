# API C Garrison.GetAvailableMissions

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of available follower missions.
 info = C_Garrison.GetAvailableMissions([missionList,] garrFollowerTypeID)

==Arguments==
:;missionList:{{apitype|MissionInfo[]?}} - ''(Not sure what the purpose is, maybe some filtering)''
:;garrFollowerTypeID:{{apitype|Enum.GarrisonFollowerType}}
{{:Enum.GarrisonFollowerType|nocaption=1}}

==Returns==
:;info:{{apitype|MissionInfo[]}}
{{:Struct_MissionInfo|nocaption=1}}

==Example==
<syntaxhighlight lang="lua">
-- /dump C_Garrison.GetAvailableMissions(Enum.GarrisonFollowerType.FollowerType_9_0_GarrisonFollower)
{
  [1] = {
     areaID = 10413,
     basecost = 10,
     canStart = true,
     completed = false,
     cost = 10,
     costCurrencyTypesID = 1813,
     description = "Дознаватели из архивов скрывают важные сведения о резервах анимы. Добудьте эту информацию.",
     duration = "4h",
     durationSeconds = 14400,
     followers = { ... },
     followerTypeID = 123,
     hasBonusEffect = false,
     inProgress = false,
     iLevel = 800,
     isTutorialMission = false,
     isMaxLevel = true,
     isRare = false,
     isZoneSupport = false,
     level = 60,
     location = "Revendreth",
     locTextureKit = "GarrMissionLocation-Revendreth",
     mapPosX = 0,
     mapPosY = 0,
     missionID = 2243,
     missionScalar = 49,
     name = "Дознание среди дознавателей",
     numFollowers = 5,
     offeredGarrMissionTextureID = 0,
     offerEndTime = 824530.75,
     offerTimeRemaining = "6h 27min",
     overmaxRewards = { ... },
     overmaxSucceeded = false,
     requiredChampionCount = 1,
     requiredSuccessChance = 0,
     rewards = { ... },
     type = "9.0 Encounter - Revendreth",
     typeAtlas = "BfAMission-Icon-QuickStrike",
     xp = 500,
  }, -- [1]
  ...
}
</syntaxhighlight>

<!-- luals
---@param garrFollowerTypeID Enum.GarrisonFollowerType
---@return MissionInfo[] info
---@overload fun(missionList: MissionInfo[], garrFollowerTypeID: Enum.GarrisonFollowerType)
function C_Garrison.GetAvailableMissions(garrFollowerTypeID) end

---@class MissionInfo
---@field areaID number
---@field basecost number
---@field canStart boolean
---@field completed boolean
---@field cost number
---@field costCurrencyTypesID number
---@field description string
---@field duration string
---@field durationSeconds number
---@field followers table
---@field followerTypeID Enum.GarrisonFollowerType
---@field hasBonusEffect boolean
---@field iLevel number
---@field inProgress boolean
---@field isMaxLevel boolean
---@field isRare boolean
---@field isTutorialMission boolean
---@field isZoneSupport boolean
---@field level number
---@field location string
---@field locTextureKit string
---@field mapPosX number
---@field mapPosY number
---@field missionEndTime? number
---@field missionID number
---@field missionScalar number
---@field name string
---@field numFollowers number
---@field offeredGarrMissionTextureID number
---@field offerEndTime number
---@field offerTimeRemaining string
---@field overmaxRewards MissionOvermaxRewards
---@field overmaxSucceeded boolean
---@field requiredChampionCount number
---@field requiredSuccessChance number
---@field rewards MissionRewards
---@field timeLeft? string
---@field timeLeftSeconds? number
---@field type string
---@field typeAtlas string
---@field xp number

---@class MissionOvermaxRewards
---@field followerXP number
---@field icon string
---@field name string
---@field title string
---@field tooltip string

---@class MissionRewards
---@field currencyID number
---@field icon number
---@field quantity number
---@field title string
-->
```