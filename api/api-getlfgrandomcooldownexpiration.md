# API GetLFGRandomCooldownExpiration

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the time at which you may once again queue for a random dungeon.
 expiryTime = GetLFGRandomCooldownExpiration()

==Returns==
:;expiryTime:{{apitype|number?}} - time ({{api|GetTime}}() value) at which you may once again queue for a random dungeon if you're currently unable to do so, nil otherwise.

==Patch changes==
* {{Patch 3.3.3|note=Added.}}

==See also==
* {{api|GetLFGDeserterExpiration}}
* {{api|UnitHasLFGRandomCooldown}}
```