# API GetRealZoneText

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the map instance name.
 zone = GetRealZoneText([instanceID])

==Arguments==
:;instanceID:{{apitype|number?}}  : [[InstanceID]] - When omitted, returns current instanceID name.

==Returns==
:;zone:{{apitype|string}} - The name of the map instance.

==Details==
* Returns the name of the map instance which can be different from {{api|GetZoneText}}()
* The returned zone name is localized to the game client's language.

==Example==
Returns the current zone.
 /dump GetRealZoneText()
 > "Stormwind City"

Returns the name of a specific instanceID.
 /dump GetRealZoneText(451)
 > "Development Land"
```