# API GetDeathRecapLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a chat link for a specific death.
 recapLink = GetDeathRecapLink(recapID)

==Arguments==
:;recapID:{{apitype|number}} - The specific death to view, from 1 to the most recent death.

==Returns==
:;recapLink:{{apitype|string}} : [[Hyperlinks#death|deathLink]]

==Patch changes==
* {{Patch 6.1.0|note=Added}}

==See also==
* {{api|DeathRecap_HasEvents}}
* {{api|DeathRecap_GetEvents}}
```