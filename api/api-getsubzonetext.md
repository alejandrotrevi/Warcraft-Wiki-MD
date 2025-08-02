# API GetSubZoneText

**Contributor:** Rhodan46

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the subzone name.
 subzone = GetSubZoneText()

==Returns==
:;subzone:{{apitype|string}} - Subzone name or an empty string (if not in a subzone).

==Example==
Returns the subzone name where the player is currently located. If not in a subzone, it returns an empty string.

 /run print("Current SubZone: " .. GetSubZoneText())

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|ZONE_CHANGED_INDOORS}} }}
|}
```