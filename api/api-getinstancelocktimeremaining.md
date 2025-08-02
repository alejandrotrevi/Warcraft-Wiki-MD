# API GetInstanceLockTimeRemaining

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the instance lock timer for the current instance.
 lockTimeleft, isPreviousInstance, encountersTotal, encountersComplete = GetInstanceLockTimeRemaining()

==Returns==
:;lockTimeLeft:{{apitype|number}} - Seconds until lock period ends.
:;isPreviousInstance:{{apitype|boolean}} - Whether this instance has yet to be entered since last lockout expired (allowing for lock extension options).
:;encountersTotal:{{apitype|number}} - Total number of bosses in the instance.
:;encountersComplete:{{apitype|number}} - Number of bosses already dead in the instance.

==Details==
* On the continent of Pandaria, unlike other open world continents, <code>encountersTotal</code> is reported as 4. According to {{api|GetInstanceLockTimeRemainingEncounter}}, this corresponds with the first 4 Pandaria world bosses of the expansion - [[Salyis's Warband|Galleon]], [[Sha of Anger]],  [[Nalak]], and [[Oondasta]]. 
* As of patch 5.4, the new world boss system isolates non-instance lockouts to {{api|GetNumSavedWorldBosses}} and {{api|GetSavedWorldBossInfo}}. It is likely that interacting with those bosses or their loot no longer has any effect on the old instance-based system represented by this function.

==Patch changes==
* {{Patch 3.2.0|note=<code>isPreviousInstance</code> return value added.}}

==See also==
* {{api|GetInstanceLockTimeRemainingEncounter}}(...) - drills down to specific boss
* {{api|GetSavedInstanceInfo}}(...) - newer, expanded version of this function
```