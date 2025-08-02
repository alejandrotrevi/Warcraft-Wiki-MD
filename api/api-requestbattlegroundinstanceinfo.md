# API RequestBattlegroundInstanceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests the available instances of a battleground.
 RequestBattlegroundInstanceInfo(index)

==Arguments==
:;index:{{apitype|number}} - Index of the battleground type to request instance information for; valid indices start from 1 and go up to {{api|GetNumBattlegroundTypes}}().

==Triggers events==
* {{api|t=e|PVPQUEUE_ANYWHERE_SHOW}} is fired when the requested information becomes available.

==Details==
* Calling {{api|JoinBattlefield}} after calling this function, but before {api|t=e|PVPQUEUE_ANYWHERE_SHOW}}, will fail silently; you must wait for the instance list to become available before you can queue for an instance.

==See Also==
* {{api|GetNumBattlefields}}
* {{api|GetBattlefieldInfo}}
```