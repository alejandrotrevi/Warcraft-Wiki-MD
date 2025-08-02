# API GetBattlefieldInstanceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the battlefield instance ID for an index in the battlemaster listing.
 instanceID = GetBattlefieldInstanceInfo(index)

==Arguments==
:;index:{{apitype|number}} - The battlefield instance index, from 1 to {{api|GetNumBattlefields}}() when speaking to the battlemaster.

==Returns==
:;instanceID:{{apitype|number}} - The battlefield instance ID. For example the ID in <code>"Warsong Gulch 2"</code>

==Patch changes==
* {{Patch 4.0.1|note=Removed.}}
* {{Patch 1.4.0|note=Added.}}
```