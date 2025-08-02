# API C ClubFinder.GetStatusOfPostingFromClubId

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 postingFlags = C_ClubFinder.GetStatusOfPostingFromClubId(postingID)

==Arguments==
:;postingID:{{apitype|string}}

==Returns==
:;postingFlags:{{apitype|number}} - Enum.ClubFinderClubPostingStatusFlags[]
{| class="sortable darktable zebra"
! Value !! Field !! Description
|-
| <center>0</center> || None ||
|-
| <center>1</center> || NeedsCacheUpdate ||
|-
| <center>2</center> || ForceDescriptionChange ||
|-
| <center>3</center> || ForceNameChange ||
|-
| <center>4</center> || UnderReview ||
|-
| <center>5</center> || Banned ||
|-
| <center>6</center> || FakePost ||
|-
| <center>7</center> || PendingDelete ||
|-
| <center>8</center> || PostDelisted ||
|}

==Patch changes==
* {{Patch 8.2.5|note=Added. (Build 32494 Nov 11 2019)}}
```