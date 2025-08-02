# API C PetBattles.SetPendingReportTargetFromUnit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Starts the process of reporting the specified battle pet for having a bad name.
 C_PetBattles.SetPendingReportTargetFromUnit(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Details==
Needs to be followed up with <code>StaticPopup_Show("CONFIRM_REPORT_BATTLEPET_NAME", name)</code> OR <code>{{api|ReportPlayer}}(PLAYER_REPORT_TYPE_BAD_BATTLEPET_NAME, "pending")</code> to complete the reporting process.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.SetPendingReportBattlePetTarget}} - if you want to report a battle pet in the current pet battle
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```