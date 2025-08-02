# API UnitPVPName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the unit's name with title (e.g. "Bob the Explorer").
 titleName = UnitPVPName(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to retrieve the name and title of.

==Returns==
:;titleName:{{apitype|string}} - The unit's combined title and name, e.g. "Playername, the Insane", or nil if the unit is out of range.

==Details==
* This function retrieves information about all titles; at the time it was added, titles were exclusively gained through PvP rankings.
* Note that <code>titleName</code> can be nil if the unit is not currently {{api|UnitIsVisible|visible}} to the client.
```