# API GetPartyAssignment

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if a group member is assigned the main tank/assist role.
 isAssigned = GetPartyAssignment(assignment [, raidmember [, exactMatch]])

==Arguments==
:;assignment:{{apitype|string}} - The role to search, either "MAINTANK" or "MAINASSIST" (not case-sensitive).
:;raidmember:{{apitype|string?}} : [[UnitId]]
:;exactMatch:{{apitype|boolean?}}

==Returns==
:;isAssigned:{{apitype|boolean}}

==Patch changes==
* {{Patch 2.0.1|note=Added.}}
```