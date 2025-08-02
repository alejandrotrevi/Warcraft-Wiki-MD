# API C GuildInfo.IsGuildRankAssignmentAllowed

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GuildInfo|system=GuildInfo}}
Needs summary.
 isGuildRankAssignmentAllowed = C_GuildInfo.IsGuildRankAssignmentAllowed(guid, rankOrder)

==Arguments==
:;guid:{{apitype|string}}
:;rankOrder:{{apitype|number}} - Starting at 1 (Guild Master)

==Returns==
:;isGuildRankAssignmentAllowed:{{apitype|boolean}}

==Patch changes==
* {{Patch 8.1.0|note=Added <code>isGuildRankAssignmentAllowed</code> return.}}
* {{Patch 8.0.1|note=Added <code>C_GuildInfo.IsGuildRankAssignmentAllowed()</code>}}
* {{Patch 4.1.0|note=Added {{api|IsGuildRankAssignmentAllowed}}()}}
```