# API C Item.GetDelvePreviewItemLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Needs summary.
 itemLink = C_Item.GetDelvePreviewItemLink(itemID, context)

==Arguments==
:;itemID:{{apitype|number}}
:;context:{{apitype|Enum.ItemCreationContext}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|None}} || 
|-
| 1 || {{apiname|DungeonNormal}} || 
|-
| 2 || {{apiname|DungeonHeroic}} || 
|-
| 3 || {{apiname|RaidNormal}} || 
|-
| 4 || {{apiname|RaidFinder}} || 
|-
| 5 || {{apiname|RaidHeroic}} || 
|-
| 6 || {{apiname|RaidMythic}} || 
|-
| 7 || {{apiname|PvPUnranked_1}} || 
|-
| 8 || {{apiname|PvPRanked_1}} || 
|-
| 9 || {{apiname|ScenarioNormal}} || 
|-
| 10 || {{apiname|ScenarioHeroic}} || 
|-
| 11 || {{apiname|QuestReward}} || 
|-
| 12 || {{apiname|Store}} || 
|-
| 13 || {{apiname|TradeSkill}} || 
|-
| 14 || {{apiname|Vendor}} || 
|-
| 15 || {{apiname|BlackMarket}} || 
|-
| 16 || {{apiname|ChallengeMode_1}} || 
|-
| 17 || {{apiname|DungeonLevelUp_1}} || 
|-
| 18 || {{apiname|DungeonLevelUp_2}} || 
|-
| 19 || {{apiname|DungeonLevelUp_3}} || 
|-
| 20 || {{apiname|DungeonLevelUp_4}} || 
|-
| 21 || {{apiname|ForceNone}} || 
|-
| 22 || {{apiname|Timewalker}} || 
|-
| 23 || {{apiname|DungeonMythic}} || 
|-
| 24 || {{apiname|PvPHonorReward}} || 
|-
| 25 || {{apiname|WorldQuest_1}} || 
|-
| 26 || {{apiname|WorldQuest_2}} || 
|-
| 27 || {{apiname|WorldQuest_3}} || 
|-
| 28 || {{apiname|WorldQuest_4}} || 
|-
| 29 || {{apiname|WorldQuest_5}} || 
|-
| 30 || {{apiname|WorldQuest_6}} || 
|-
| 31 || {{apiname|MissionReward_1}} || 
|-
| 32 || {{apiname|MissionReward_2}} || 
|-
| 33 || {{apiname|ChallengeMode_2}} || 
|-
| 34 || {{apiname|ChallengeMode_3}} || 
|-
| 35 || {{apiname|ChallengeModeJackpot}} || 
|-
| 36 || {{apiname|WorldQuest_7}} || 
|-
| 37 || {{apiname|WorldQuest_8}} || 
|-
| 38 || {{apiname|PvPRanked_2}} || 
|-
| 39 || {{apiname|PvPRanked_3}} || 
|-
| 40 || {{apiname|PvPRanked_4}} || 
|-
| 41 || {{apiname|PvPUnranked_2}} || 
|-
| 42 || {{apiname|WorldQuest_9}} || 
|-
| 43 || {{apiname|WorldQuest_10}} || 
|-
| 44 || {{apiname|PvPRanked_5}} || 
|-
| 45 || {{apiname|PvPRanked_6}} || 
|-
| 46 || {{apiname|PvPRanked_7}} || 
|-
| 47 || {{apiname|PvPUnranked_3}} || 
|-
| 48 || {{apiname|PvPUnranked_4}} || 
|-
| 49 || {{apiname|PvPUnranked_5}} || 
|-
| 50 || {{apiname|PvPUnranked_6}} || 
|-
| 51 || {{apiname|PvPUnranked_7}} || 
|-
| 52 || {{apiname|PvPRanked_8}} || 
|-
| 53 || {{apiname|WorldQuest_11}} || 
|-
| 54 || {{apiname|WorldQuest_12}} || 
|-
| 55 || {{apiname|WorldQuest_13}} || 
|-
| 56 || {{apiname|PvPRankedJackpot}} || 
|-
| 57 || {{apiname|TournamentRealm}} || 
|-
| 58 || {{apiname|Relinquished}} || 
|-
| 59 || {{apiname|LegendaryForge}} || 
|-
| 60 || {{apiname|QuestBonusLoot}} || 
|-
| 61 || {{apiname|CharacterBoost_1}} || 
|-
| 62 || {{apiname|CharacterBoost_2}} || 
|-
| 63 || {{apiname|LegendaryCrafting_1}} || 
|-
| 64 || {{apiname|LegendaryCrafting_2}} || 
|-
| 65 || {{apiname|LegendaryCrafting_3}} || 
|-
| 66 || {{apiname|LegendaryCrafting_4}} || 
|-
| 67 || {{apiname|LegendaryCrafting_5}} || 
|-
| 68 || {{apiname|LegendaryCrafting_6}} || 
|-
| 69 || {{apiname|LegendaryCrafting_7}} || 
|-
| 70 || {{apiname|LegendaryCrafting_8}} || 
|-
| 71 || {{apiname|LegendaryCrafting_9}} || 
|-
| 72 || {{apiname|WeeklyRewardsAdditional}} || 
|-
| 73 || {{apiname|WeeklyRewardsConcession}} || 
|-
| 74 || {{apiname|WorldQuestJackpot}} || 
|-
| 75 || {{apiname|NewCharacter}} || 
|-
| 76 || {{apiname|WarMode}} || 
|-
| 77 || {{apiname|PvPBrawl_1}} || 
|-
| 78 || {{apiname|PvPBrawl_2}} || 
|-
| 79 || {{apiname|Torghast}} || 
|-
| 80 || {{apiname|CorpseRecovery}} || 
|-
| 81 || {{apiname|WorldBoss}} || 
|-
| 82 || {{apiname|RaidNormalExtended}} || 
|-
| 83 || {{apiname|RaidFinderExtended}} || 
|-
| 84 || {{apiname|RaidHeroicExtended}} || 
|-
| 85 || {{apiname|RaidMythicExtended}} || 
|-
| 86 || {{apiname|CharacterBoost_3}} || 
|-
| 87 || {{apiname|ChallengeMode_4}} || 
|-
| 88 || {{apiname|PvPRanked_9}} || 
|-
| 89 || {{apiname|RaidNormalExtended_2}} || 
|-
| 90 || {{apiname|RaidFinderExtended_2}} || 
|-
| 91 || {{apiname|RaidHeroicExtended_2}} || 
|-
| 92 || {{apiname|RaidMythicExtended_2}} || 
|-
| 93 || {{apiname|RaidNormalExtended_3}} || 
|-
| 94 || {{apiname|RaidFinderExtended_3}} || 
|-
| 95 || {{apiname|RaidHeroicExtended_3}} || 
|-
| 96 || {{apiname|RaidMythicExtended_3}} || 
|-
| 97 || {{apiname|TemplateCharacter_1}} || 
|-
| 98 || {{apiname|TemplateCharacter_2}} || 
|-
| 99 || {{apiname|TemplateCharacter_3}} || 
|-
| 100 || {{apiname|TemplateCharacter_4}} || 
|-
| 101 || {{apiname|DungeonNormalJackpot}} || 
|-
| 102 || {{apiname|DungeonHeroicJackpot}} || 
|-
| 103 || {{apiname|DungeonMythicJackpot}} || 
|-
| 104 || {{apiname|Delves_1}} || 
|-
| 105 || {{apiname|Timerunning}} || 
|-
| 106 || {{apiname|Delves_2}} || 
|-
| 107 || {{apiname|Delves_3}} || 
|-
| 108 || {{apiname|DelvesJackpot}} || 
|}

==Returns==
:;itemLink:{{apitype|string?}}
```