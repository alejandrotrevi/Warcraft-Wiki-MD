# API GetTrainerServiceTypeFilter

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the status of a skill filter in the trainer window.
 status = GetTrainerServiceTypeFilter(type)

==Arguments==
:;type:{{apitype|string}} - Possible values: 
::*"available"
::*"unavailable"
::*"used" (already known)

==Returns==
:;status:{{apitype|boolean}} - true if currently displaying trainer services of the specified type, false otherwise.

==Patch changes==
* {{Patch 6.0.2|note=Returns a boolean value instead of 0/1.}}
```