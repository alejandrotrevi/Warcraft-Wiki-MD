# API C Garrison.MissionBonusRoll

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Receives mission loot.
 C_Garrison.MissionBonusRoll(missionID)

==Arguments==
:;missionID:{{apitype|number}}

==Details==
* Used after {{api|C_Garrison.MarkMissionComplete}}() and {{api|t=e|GARRISON_MISSION_COMPLETE_RESPONSE}}.
* Fires {{api|t=e|GARRISON_MISSION_BONUS_ROLL_COMPLETE}}. <!--  Does this also fire the other GARRISON_MISSION_BONUS_ROLL_XXX events, or do they happen first to indicate mission loot is available? -->

==Example==
Silently completes all Shadowlands missions:
<syntaxhighlight lang="lua">
for __, mission in pairs(C_Garrison.GetCompleteMissions(123)) do
	C_Garrison.MarkMissionComplete(mission.missionID)
    C_Garrison.MissionBonusRoll(mission.missionID)
end
</syntaxhighlight>
```