# API GetLFGDeserterExpiration

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the time at which you may once again use the dungeon finder after prematurely leaving a group.
 expiryTime = GetLFGDeserterExpiration()

==Returns==
:;expiryTime:{{apitype|number?}} - time ({{api|GetTime}}() value) at which you may once again use the dungeon finder; nil if you're not currently under the effects of the deserter penalty.

==Patch changes==
* {{Patch 3.3.3|note=Added.}}

==See also==
* {{api|GetLFGRandomCooldownExpiration}}
* {{api|UnitHasLFGDeserter}}
```