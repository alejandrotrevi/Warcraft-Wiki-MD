# API C ReportSystem.OpenReportPlayerDialog

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Opens the dialog for reporting a player.
 C_ReportSystem.OpenReportPlayerDialog(reportType, playerName [, playerLocation])

==Arguments==
:;reportType:{{apitype|string}} - One of the strings found in <code>PLAYER_REPORT_TYPE</code>
:;playerName:{{apitype|string}} - Name of the player being reported
:;playerLocation:{{apitype|PlayerLocationMixin}}
{{Collapse|Const PLAYER_REPORT_TYPE}}

==Details==
* This function is not protected and therefore available to Addons, unlike {{api|C_ReportSystem.InitiateReportPlayer}} and {{api|C_ReportSystem.SendReportPlayer}}
* This reporting restriction was added because AddOn [https://www.curseforge.com/wow/addons/bad-boy BadBoy] allegedly sent out a number of false positives. <ref>{{ref web|title=IRC log for #wowuidev on 20190424|url=http://infobot.rikers.org/%23wowuidev/20190424.html.gz|date=20190424}}</ref>
* Triggers {{api|t=e|OPEN_REPORT_PLAYER}} once the window is open

==Example==
* Opens the spam report dialog for the current target.
 /run C_ReportSystem.OpenReportPlayerDialog(PLAYER_REPORT_TYPE_SPAM, UnitName("target"), PlayerLocation:CreateFromUnit("target"))

==Patch changes==
* {{Patch 8.2.0|note=Added.}}

==References==
```