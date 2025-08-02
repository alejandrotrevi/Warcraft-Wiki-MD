# API GetInstanceLockTimeRemainingEncounter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about bosses in the instance the player is about to be saved to.
 bossName, texture, isKilled = GetInstanceLockTimeRemainingEncounter(id)

==Arguments==
:;id:{{apitype|number}} - Index of the boss to query, ascending from 1 to encountersTotal return value from {{api|GetInstanceLockTimeRemaining}}.

==Returns==
:;bossName:{{apitype|string}} - Name of the boss.
:;texture:{{apitype|string}} - ?
:;isKilled:{{apitype|boolean}} - true if the boss has been killed.

==See also==
* {{api|GetInstanceLockTimeRemaining}}() - zooms out to full instance's info
* {{api|GetSavedWorldBossInfo}}(...) - also provides boss info, but for world bosses
```