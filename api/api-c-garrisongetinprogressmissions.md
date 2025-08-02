# API C Garrison.GetInProgressMissions

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of active follower missions.
 info = C_Garrison.GetInProgressMissions(garrFollowerTypeID)

==Arguments==
:;garrFollowerTypeID:{{apitype|Enum.GarrisonFollowerType}}
{{:Enum.GarrisonFollowerType|nocaption=1}}

==Returns==
:;info:{{apitype|MissionInfo[]}}
{{:Struct_MissionInfo|nocaption=1}}

==Example==
<syntaxhighlight lang="lua">
-- /dump C_Garrison.GetInProgressMissions(Enum.GarrisonFollowerType.FollowerType_9_0)
{
  [1] = {
      areaID = 11510,
      basecost = 50,
      canStart = false,
      completed = false,
      cost = 50,
      costCurrencyTypesID = 1813,
      description = "Дейфир обуздал свою гордыню и обрел союзников в борьбе. Желаю тебе удачи.",
      duration = "14h",
      durationSeconds = 50400,
      followers = { ... },
      followerTypeID = 123,
      hasBonusEffect = false,
      iLevel = 800,
      inProgress = true,
      isMaxLevel = true,
      isRare = false,
      isTutorialMission = false,
      isZoneSupport = false,
      level = 60,
      location = "Ardenweald",
      locTextureKit = "GarrMissionLocation-Ardenweald",
      mapPosX = 0,
      mapPosY = 0,
      missionEndTime = 1616376750,
      missionID = 2190,
      missionScalar = 47,
      name = "Дейфир возвращается",
      numFollowers = 5,
      offeredGarrMissionTextureID = 0,
      overmaxRewards = { ... },
      overmaxSucceeded = false,
      requiredChampionCount = 1,
      requiredSuccessChance = 0,
      rewards = { ... },
      timeLeft = "0s",
      timeLeftSeconds = 0,
      type = "9.0 Encounter - Ardenweald",
      typeAtlas = "ShipMissionIcon-Legendary-Map",
      xp = 1200,
  }, -- [1]
  ...
}
</syntaxhighlight>
```