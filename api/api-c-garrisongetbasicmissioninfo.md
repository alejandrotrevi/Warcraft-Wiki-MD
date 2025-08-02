# API C Garrison.GetBasicMissionInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a table containing information on the requested mission.
 info = C_Garrison.GetBasicMissionInfo(missionID)

==Arguments==
:;missionID:{{apitype|number}}

==Returns==
:;info:{{apitype|MissionInfo}}
{{:Struct_MissionInfo|nocaption=1}}

==Example==
<syntaxhighlight lang="lua">
-- /dump C_Garrison.GetBasicMissionInfo(165)
{
	description = "Energy-siphoning water spirits are giving our spellcasters fits. Time to bring in reinforcements.",
	cost = 10,
	duration = "2 hr",
	durationSeconds = 7200,
	level = 98,
	type = "Combat",
	locPrefix = "GarrMissionLocation-Nagrand",
	rewards = {
		[527] = {
			title = "Bonus Follower XP",
			followerXP = 900,
			tooltip = "+900 XP",
			icon = "Interface\\Icons\\XPBonus_Icon",
			name = "+900 XP"
		}
	},
	numRewards = 1,
	numFollowers = 1,
	state = -2,
	iLevel = 0,
	name = "Surge Protection",
	followers = {
	},
	location = "Nagrand",
	isRare = false,
	typeAtlas = "GarrMission_MissionIcon-Combat",
	missionID = 165
}
</syntaxhighlight>

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```