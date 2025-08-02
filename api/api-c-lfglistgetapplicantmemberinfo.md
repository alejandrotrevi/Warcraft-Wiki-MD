# API C LFGList.GetApplicantMemberInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns info for an applicant.
 name, class, localizedClass, level, itemLevel, honorLevel, tank, healer, damage, assignedRole, relationship, dungeonScore, pvpItemLevel = C_LFGList.GetApplicantMemberInfo(applicantID, memberIndex)

==Arguments==
:;applicantID:{{apitype|number}} - ascending number of applicants since creation of the activity returned by {{api|C_LFGList.GetApplicants}}()
:;memberIndex:{{apitype|number}} - iteration of {{api|C_LFGList.GetApplicants}}() argument #4 (numMembers)

==Returns==
:;1. name:{{apitype|string}} - Character name and realm
:;2. class:{{apitype|string}} - english class name (uppercase)
:;3. localizedClass:{{apitype|string}} - localized class name
:;4. level:{{apitype|number}}
:;5. itemLevel:{{apitype|number}}
:;6. honorLevel:{{apitype|number}}
:;7. tank:{{apitype|boolean}} - true if applicant offer tank role
:;8. healer:{{apitype|boolean}} - true if applicant offer healer role
:;9. damage:{{apitype|boolean}} - true if applicant offer damage role
:;10. assignedRole:{{apitype|string}} - english role name (uppercase)
:;11. relationship:{{apitype|boolean?}} - true if a friend otherwise nil
:;12. dungeonScore:{{apitype|number}}
:;13. pvpItemLevel:{{apitype|number}}

==Patch changes==
* {{Patch 9.1.5|note=Added <code>pvpItemLevel</code>}}
* {{Patch 9.1.0|note=Added <code>dungeonScore</code>}}
* {{Patch 7.0.3|note=Added <code>honorLevel</code>}}
* {{Patch 6.0.2|note=Added.}}
```