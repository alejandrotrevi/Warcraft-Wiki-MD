# API PromoteToLeader

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Promotes a unit to group leader.
 PromoteToLeader(unit)
 PromoteToLeader(name, exactmatch)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to promote
----
:;name:{{apitype|string}}
:;exactmatch:{{apitype|boolean}}

<!-- luals
---@param unit UnitToken
---@overload fun(name: string, exactmatch: boolean)
function PromoteToLeader(unit) end
-->
```