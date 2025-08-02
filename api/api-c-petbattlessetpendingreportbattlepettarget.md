# API C PetBattles.SetPendingReportBattlePetTarget

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Starts the process of reporting one of your opponent's battle pets for having a bad name.
 C_PetBattles.SetPendingReportBattlePetTarget(petIndex)

==Arguments==
:;petIndex:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was its 3rd pet when it entered battle, it will always be 3 on the index.

==Details==
Needs to be followed up with <code>StaticPopup_Show("CONFIRM_REPORT_BATTLEPET_NAME", name)</code> OR <code>{{api|ReportPlayer}}(PLAYER_REPORT_TYPE_BAD_BATTLEPET_NAME, "pending")</code> to complete the reporting process.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.SetPendingReportTargetFromUnit}} - if you want to report a battle pet's name out in the world, outside of a pet battle
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```