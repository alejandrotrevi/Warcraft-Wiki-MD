# API C ReportSystem.SetPendingReportPetTarget

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Report a pet for an inappropriate name.
 set = C_ReportSystem.SetPendingReportPetTarget([target])

==Arguments==
:;target:{{apitype|string?}} : [[UnitId]] - defaults to "target".

==Returns==
:;set:{{apitype|boolean}} - whether the report was succesfully set.

==Patch changes==
* {{Patch 8.1.0|note=Moved to {{api|C_ReportSystem.SetPendingReportPetTarget}}. The previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#199]}}
* {{Patch 5.0.4|note=Added as <code>SetPendingReportPetTarget()</code>.}}
```