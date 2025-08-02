# API CombatLogSetCurrentEntry

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the currently selected combat log entry to the given value, to be retrieved using {{api|CombatLogGetCurrentEntry}}().
 isValidIndex = CombatLogSetCurrentEntry(index [, ignoreFilter])

==Arguments==
:;index:{{apitype|number}} - see details below
:;ignoreFilter:{{apitype|boolean?}} - set to true to ignore combat log filters

==Returns==
:;isValidIndex:{{apitype|boolean}} - will return false if the index does not exist in the combat log, but will still set the entry. Otherwise, returns true for valid indices.

==Details==
Combat log indexing works a bit differently than standard Lua indexing. You can treat the combat log like a big table, with the oldest entries being placed at the beginning, and the newest entries at the end.

Unlike standard Lua tables, however, an index of 0 will set the entry to the most recent combat log entry. Additionally, you are also able to index the combat log backwards using negative values. For example, an index of -1 will return the second to last, or second most recent entry in the combat log.

See {{api|CombatLogAdvanceEntry}}() for details on traversing the combat log.

==Examples==
*Combat log indexing
<syntaxhighlight lang="lua">
CombatLogSetCurrentEntry(0, true); -- most recent entry, ignoring filters.
local newestEntry = {CombatLogGetCurrentEntry()};

CombatLogSetCurrentEntry(1, true); -- oldest entry, ignoring filters.
local oldestEntry = {CombatLogGetCurrentEntry()};

CombatLogSetCurrentEntry(-5, true); -- fifth newest entry, ignoring filters.
local fifthNewestEntry = {CombatLogGetCurrentEntry()};

CombatLogSetCurrentEntry(5, true); -- fifth oldest entry, ignoring filters.
local fifthOldestEntry = {CombatLogGetCurrentEntry()};
</syntaxhighlight>

==References==
{{api|CombatLogGetCurrentEntry}}()

{{api|CombatLogAdvanceEntry}}()
```