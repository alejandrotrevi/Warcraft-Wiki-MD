# API CombatLogGetCurrentEntry

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the combat log entry that is currently selected by {{api|CombatLogSetCurrentEntry}}().
 local timestamp, subevent, hideCaster, sourceGUID, sourceName, sourceFlags, sourceRaidFlags, destGUID, destName, destFlags, destRaidFlags = CombatLogGetCurrentEntry();

==Returns==
This function's returns are identical to those of {{api|CombatLogGetCurrentEventInfo}}(). For more details see {{api|COMBAT_LOG_EVENT}}.

<!-- luals
---@return number timestamp
---@return string subevent
---@return boolean hideCaster
---@return string sourceGUID
---@return string sourceName
---@return number sourceFlags
---@return number sourceRaidFlags
---@return string destGUID
---@return string destName
---@return number destFlags
---@return number destRaidFlags
---@return any ...
function CombatLogGetCurrentEntry() end
-->
```