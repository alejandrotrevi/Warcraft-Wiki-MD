# API SetTrainerServiceTypeFilter

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the status of a skill filter in the trainer window.
 SetTrainerServiceTypeFilter(type, enable [, exclusive])

==Arguments==
:;type:{{apitype|string}} - filter to set the status for:
::*"available" (can learn)
::*"unavailable" (can't learn)
::*"used" (already known)
:;enable:{{apitype|boolean}} - true to show, false to hide items matching the specified filter. <!-- (Note that this is likely a bug as GetTrainerServiceTypeFilter returns a boolean now.) -->
:;exclusive:{{apitype|boolean}}

==Patch changes==
* {{Patch 6.0.2|note=Gained "exclusive" return.}}
```