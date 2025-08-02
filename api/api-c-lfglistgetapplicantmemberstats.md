# API C LFGList.GetApplicantMemberStats

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the [[Proving Grounds]] stats of an applicant.
 stats = C_LFGList.GetApplicantMemberStats(applicantID, memberIndex)

==Arguments==
:;applicantID:{{apitype|number}} - ascending number of applicants since creation of the activity returned by [[API C_LFGList.GetApplicants|C_LFGList.GetApplicants]]()
:;memberIndex:{{apitype|number}} - iteration of [[API C_LFGList.GetApplicants|C_LFGList.GetApplicants]]() argument #4 (numMembers)

==Returns==
:;stats:{{apitype|table}}

==Details==
* Currently used to check proving ground stats of an applicant group member

{|class="darktable" style="float:left"
! Entry !! PG Tank
|-
| stats[23690]>0 || Gold
|-
| stats[23687]>0 || Silver
|-
| stats[23684]>0 || Bronze
|}

{|class="darktable" style="float:left"
! Entry !! PG Healer
|-
| stats[23691]>0 || Gold
|-
| stats[23688]>0 || Silver
|-
| stats[23685]>0 || Bronze
|}

{|class="darktable" style="float:left"
! Entry !! PG Damage
|-
| stats[23689]>0 || Gold
|-
| stats[23686]>0 || Silver
|-
| stats[23683]>0 || Bronze
|}
{{clear}}

==See also==
* [[API C_LFGList.GetApplicants|C_LFGList.GetApplicants]]()
* [[API C_LFGList.GetApplicantMemberInfo|C_LFGList.GetApplicantMemberInfo]](applicantID)
```