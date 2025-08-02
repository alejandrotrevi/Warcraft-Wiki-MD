# API C ReportSystem.GetMinorCategoriesForReportTypeAndMajorCategory

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ReportSystem|system=ReportSystem}}
Needs summary.
 minorCategories = C_ReportSystem.GetMinorCategoriesForReportTypeAndMajorCategory(reportType, majorCategory)

==Arguments==
:;reportType:{{apitype|Enum.ReportType}}
{{:Enum.ReportType|nocaption=1}}
:;majorCategory:{{apitype|Enum.ReportMajorCategory}}
{{:Enum.ReportMajorCategory|nocaption=1}}

==Returns==
:;minorCategories:{{apitype|Enum.ReportMinorCategory[]}}
{{:Enum.ReportMinorCategory|nocaption=1}}

==Patch changes==
* {{Patch 9.2.5|note=Added.}}
```