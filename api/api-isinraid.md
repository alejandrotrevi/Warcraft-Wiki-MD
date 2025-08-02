# API IsInRaid

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the player is in a raid.
 isInRaid = IsInRaid([groupType])

==Arguments==
:;groupType:{{apitype|number?}} - To check for a specific type of group, provide one of:
:* LE_PARTY_CATEGORY_HOME : checks for home-realm parties.
:* LE_PARTY_CATEGORY_INSTANCE : checks for instance-specific groups.

==Returns==
:;isInRaid:{{apitype|boolean}} - true if the player is currently in a <code>groupType</code> raid group (if <code>groupType</code> was not specified, true if in any type of raid), false otherwise

==Details==
This returns true in arenas if groupType is LE_PARTY_CATEGORY_INSTANCE or is unspecified.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```