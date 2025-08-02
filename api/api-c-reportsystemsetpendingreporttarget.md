# API C ReportSystem.SetPendingReportTarget

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Populates the reporting window with details about a target player.
 set = C_ReportSystem.SetPendingReportTarget([target])
     = C_ReportSystem.SetPendingReportTargetByGuid([guid])

==Arguments==
===<font color="#4ec9b0">SetPendingReportTarget</font>===
:;target:{{apitype|string?}} : [[UnitId]] - defaults to "target"
===<font color="#4ec9b0">SetPendingReportTargetByGuid</font>===
:;guid:{{apitype|string?}} : [[GUID]]

==Returns==
:;set:{{apitype|boolean}} - whether the report was succesfully set.

==Patch changes==
* {{Patch 8.1.0|note=Moved to {{api|C_ReportSystem.SetPendingReportTarget}}. The previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#202]}}
* {{Patch 4.3.4|note=Added as {{api|SetPendingReportTarget}}.}}
```