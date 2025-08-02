# API GetWatchedFactionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the currently watched faction.
 name, standing, min, max, value, factionID = GetWatchedFactionInfo()

==Returns==
:;name:{{apitype|string}} - The name of the faction curretly being watched, nil if no faction is being watched.
:;standing:{{apitype|number}} - The [[API TYPE StandingId|StandingId]] with the faction.
:;min:{{apitype|number}} - The minimum bound for the current standing, for instance 21000 for Revered.
:;max:{{apitype|number}} - The maximum bound for the current standing, for instance 42000 for Revered.
:;value:{{apitype|number}} - The current faction level, within the bounds.
:;factionID:{{apitype|number}} ([[FactionID]]) - Unique numeric identifier for the faction.

==Patch changes==
* {{Patch 5.0.4|note=Added <code>factionID</code> return value.}}
* {{Patch 1.10.0|note=Added.}}
```