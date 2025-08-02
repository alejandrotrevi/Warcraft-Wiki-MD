# API IsFactionInactive

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the specified faction is marked inactive.
 inactive = IsFactionInactive(index)

==Arguments==
:;index:{{apitype|number}} - index of the faction within the faction list, ascending from 1.

==Returns==
:;inactive:{{apitype|boolean}} - 1 if the faction is flagged as inactive, nil otherwise.

==Patch changes==
* {{Patch 1.10.0|note=Added.}}

==See also==
* {{api|SetFactionInactive}}
* {{api|SetFactionActive}}
```