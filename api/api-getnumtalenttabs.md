# API GetNumTalentTabs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the total number of talent tabs for the player.
 numTabs = GetNumTalentTabs([isInspect])

==Arguments==
:;isInspect:{{apitype|boolean}} - Optional, will return the number of talent tabs for the current inspect target if true (see {{api|NotifyInspect}}).

==Returns==
:;numTabs:{{apitype|number}} - The number of talent tabs available (for example Elemental, Enhancement, and Restoration for Shamans).

==Patch changes==
* {{Patch 5.0.4|note=Removed.}}
* {{Patch 2.3.0|note=Added <code>inspect, pet</code> arguments.}}
```