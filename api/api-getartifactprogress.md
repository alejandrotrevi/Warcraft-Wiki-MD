# API GetArtifactProgress

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns progress info for the selected Archaeology artifact.
 numFragmentsCollected, numFragmentsAdded, numFragmentsRequired = GetArtifactProgress()

==Returns==
:;numFragmentsCollected:{{apitype|number}} - Number of collected fragments for selected artifact.
:;numFragmentsAdded:{{apitype|number}} - Number of fragments currently added through keystones for selected artifact.
:;numFragmentsRequired:{{apitype|number}} - Number of fragments required to solve the selected artifact.

==Example==
My selected Project requires 45 fragments, i have 22 fragments and a [[Keystone]] slot which i do not use.
<big>'''Result'''</big>
22 0 45
The same project, this time the [[Keystone]] slot is used.
<big>'''Result'''</big>
22 12 45

==Patch changes==
* {{Patch 4.0.1|note=Added.}}

==See also==
: [[API SetSelectedArtifact|SetSelectedArtifact]](raceIndex)
```