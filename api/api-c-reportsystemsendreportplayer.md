# API C ReportSystem.SendReportPlayer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Sends an initiated report against a player.
 C_ReportSystem.SendReportPlayer(token [, comment])

==Arguments==
;token : <span class="apitype">number</span> - the token from {{api|C_ReportSystem.InitiateReportPlayer}}.
;comment : <span title="nilable"><span class="apitype">string</span>?</span> - any comments and details.

==Patch changes==
* {{Patch 8.2.0|note=Protected. See {{api|C_ReportSystem.OpenReportPlayerDialog}}.}}
* {{Patch 8.1.5|note=Added. Partly replaces {{api|C_ChatInfo.ReportPlayer}} which is deprecated. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#205]}}
```