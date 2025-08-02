# API C LFGList.GetApplicantInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns status informations and custom message of an applicant.
 applicantData = C_LFGList.GetApplicantInfo(applicantID)

==Arguments==
:;applicantID:{{apitype|number}} - Ascending number of applicants since creation of the activity.

==Returns==
:;applicantData:{{apitype|LfgApplicantData}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|applicantID}} || {{apitype|number}} || Same as applicantID or nil
|-
| {{apiname|applicationStatus}} || {{apitype|string}} || 
|-
| {{apiname|pendingApplicationStatus}} || {{apitype|string?}} || "applied", "cancelled"
|-
| {{apiname|numMembers}} || {{apitype|number}} || 1 or higher if a group
|-
| {{apiname|isNew}} || {{apitype|boolean}} || 
|-
| {{apiname|comment}} || {{apitype|kstringLfgListApplicant}} || Applicant custom message
|-
| {{apiname|displayOrderID}} || {{apitype|number}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ applicationStatus
|-
! Value !! Description
|-
| applied || 
|-
| invited || 
|-
| failed || 
|-
| cancelled || 
|-
| declined || 
|-
| declined_full || 
|-
| declined_delisted || 
|-
| timedout || 
|-
| inviteaccepted || 
|-
| invitedeclined || 
|}

==Patch changes==
* {{Patch 8.1.0|note=Return parameters changed to structure.}}
* {{Patch 6.0.2|note=Added.}}
```