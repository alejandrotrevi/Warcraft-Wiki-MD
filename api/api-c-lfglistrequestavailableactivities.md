# API C LFGList.RequestAvailableActivities

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Signals the server to request that it send the client information about available activities.
 C_LFGList.RequestAvailableActivities()

==Triggers events==
* {{api|t=e|LFG_LIST_AVAILABILITY_UPDATE}}, when this information is available to the client

==Details==
* This is a prerequisite for at least some of the C_LFGList.GetAvailable* functions to return meaningful data.

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```