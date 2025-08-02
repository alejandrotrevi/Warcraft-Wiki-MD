# API C Reputation.IsFactionParagon

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns true if a faction is a paragon reputation.
 isParagon = C_Reputation.IsFactionParagon(factionID)

==Arguments==
:;factionID:{{apitype|number}} - The [[factionID]] from the 14th return of [[API_GetFactionInfo|GetFactionInfo]] or the 6th return from [[API_GetWatchedFactionInfo|GetWatchedFactionInfo]].

==Returns==
:;isParagon:{{apitype|boolean}} - true if the faction is Paragon level, false otherwise.

==Patch changes==
* {{Patch 7.2.0|note=Added.}}

==See also==
* {{api|GetFactionInfo}}
* {{api|GetWatchedFactionInfo}}
* {{api|C_Reputation.GetFactionParagonInfo}}
```