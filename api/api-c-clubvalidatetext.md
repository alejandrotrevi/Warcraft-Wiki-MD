# API C Club.ValidateText

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Club|system=Club}}
Needs summary.
 result = C_Club.ValidateText(clubType, text, clubFieldType)

==Arguments==
:;clubType:{{apitype|Enum.ClubType}}
{{:Enum.ClubType|nocaption=1}}
:;text:{{apitype|string}}
:;clubFieldType:{{apitype|Enum.ClubFieldType}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || ClubName || 
|-
| 1 || ClubShortName || 
|-
| 2 || ClubDescription || 
|-
| 3 || ClubBroadcast || 
|-
| 4 || ClubStreamName || 
|-
| 5 || ClubStreamSubject || 
|-
| 6 || NumTypes || 
|}

==Returns==
:;result:{{apitype|Enum.ValidateNameResult}}
{{:Enum.ValidateNameResult|nocaption=1}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```