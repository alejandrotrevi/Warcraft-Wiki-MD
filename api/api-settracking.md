# API SetTracking

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets a minimap tracking method.
 SetTracking(id,enabled)

==Parameters==
===Arguments===
:;id:The id of the tracking you would like to change. The id is assigned by the client, 1 is the first tracking method available on the tracking list, 2 is the next and so on. To get Information about a specific id, use [[API GetTrackingInfo|GetTrackingInfo]].
:;enabled:{{apitype|boolean}} flag if the specified tracking id is to be enabled or disabled.

==Example==
Enables the first tracking method on the list:
 SetTracking(1,true);
```