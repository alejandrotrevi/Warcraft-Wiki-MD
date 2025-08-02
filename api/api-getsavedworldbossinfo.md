# API GetSavedWorldBossInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the player's [[world boss]] loot lockout.
 name, worldBossID, reset = GetSavedWorldBossInfo(index)

==Arguments==
:;index:{{apitype|number}} - Index of the world boss lockout to query, ascending from 1 to {{api|GetNumSavedWorldBosses}}().

==Returns==
:;name:{{apitype|string}} - world boss lockout name, e.g. "The Four Celestials"
:;worldBossID:{{apitype|number}} - unique world boss ID, e.g. 5 for ''The Four Celestials''.
:;reset:{{apitype|number}} - time in seconds until the loot lockout expires.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|GetNumSavedWorldBosses}}() - counts number of world bosses this function applies to
* {{api|GetSavedInstanceInfo}}(...) - same function as this, but for instances
* {{api|GetInstanceLockTimeRemainingEncounter}}(...) - also gets boss info (i.e. name), but within an instance
```