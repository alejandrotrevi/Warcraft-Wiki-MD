# API InGuildParty

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether or not you are in a guild party.

'''''Usage''''':
 inGroup, numGuildPresent, numGuildRequired, xpMultiplier = InGuildParty()

==Arguments==
None

==Returns==
:;inGroup:{{apitype|boolean}} - True if you are in a valid guild group, otherwise false.
:;numGuildPresent:{{apitype|number}} - The number of guild members currently in the group.
:;numGuildRequired:{{apitype|number}} - The total number of members required to make the group into a guild group.
:;xpMultiplier:{{apitype|number}} - The amount to multiply the Guild Experience by.
```