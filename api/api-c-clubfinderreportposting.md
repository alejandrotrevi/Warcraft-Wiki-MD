# API C ClubFinder.ReportPosting

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 C_ClubFinder.ReportPosting(reportType, clubFinderGUID, playerGUID, complaintNote)

==Arguments==
:;reportType:{{apitype|number}} - Enum.ClubFinderPostingReportType
:;clubFinderGUID:{{apitype|string}}
:;playerGUID:{{apitype|string}}
:;complaintNote:{{apitype|string}}
{| class="sortable darktable zebra"
|+ Enum.ClubFinderPostingReportType
! Value !! Field !! Description
|-
| <center>0</center> || PostersName ||
|-
| <center>1</center> || ClubName ||
|-
| <center>2</center> || PostingDescription ||
|-
| <center>3</center> || ApplicantsName ||
|-
| <center>4</center> || JoinNote ||
|}

==Patch changes==
* {{Patch 8.2.5|note=Added.}}
```