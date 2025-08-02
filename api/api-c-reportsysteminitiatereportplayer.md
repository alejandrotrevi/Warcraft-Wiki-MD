# API C ReportSystem.InitiateReportPlayer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Addons may use {{api|C_ReportSystem.OpenReportPlayerDialog}}}}
Initiates a report against a player.
 token = C_ReportSystem.InitiateReportPlayer(complaintType [, playerLocation])

==Arguments==
:;complaintType:{{apitype|string}} : PLAYER_REPORT_TYPE - the reason for reporting.
:;playerLocation:{{apitype|PlayerLocationMixin}}
{{:Const_PLAYER_REPORT_TYPE}}

==Returns==
:;token:{{apitype|number}} - the token used for {{api|C_ReportSystem.SendReportPlayer}}.

==Patch changes==
* {{Patch 8.2.0|note=Protected. See {{api|C_ReportSystem.OpenReportPlayerDialog}}.}}
* {{Patch 8.1.5|note=Partially replaced by {{api|C_ReportSystem.InitiateReportPlayer}}; the previous function is depreciated. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#205]}}
* {{Patch 8.0.1|note=Added as <code>C_ChatInfo.ReportPlayer(...)</code>.}}

==References==
```