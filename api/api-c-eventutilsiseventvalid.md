# API C EventUtils.IsEventValid

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Checks if a named event exists and can be registered for.
 valid = C_EventUtils.IsEventValid(eventName)

==Arguments==
:;eventName:{{apitype|string}} - The name of the event to query.

==Returns==
:;valid:{{apitype|boolean}} - <code>true</code> if the named event exists and can be registered for, <code>false</code> if not.

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```