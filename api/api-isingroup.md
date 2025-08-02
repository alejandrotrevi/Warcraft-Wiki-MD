# API IsInGroup

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the player is in a group.
 inGroup = IsInGroup([groupType])

==Arguments==
:;groupType:{{apitype|number?}} - If omitted, checks if you're in any type of group.
{{:LE_PARTY_CATEGORY|nocaption=1}}

==Returns==
:;inGroup:{{apitype|boolean}} - Returns true if the player is in the <code>groupType</code> group if specified, or in any type of group.

==Details==
It is possible for a character to belong to a ''home'' group at the same time they are in an ''instance'' group ([[LFR]] or [[Flexible Raid|Flex]]). To distinguish between a party and a raid, use {{api|IsInRaid}}().

==Patch changes==
* {{Patch 5.0.4|note=Added <code>groupType</code> argument.}}
```