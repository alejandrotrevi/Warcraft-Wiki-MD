# API SwapRaidSubgroup

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 4.0.1}}
Swaps two raid members into different groups.
 SwapRaidSubgroup(index1, index2)

==Arguments==
:;index1:{{apitype|number}} - ID of first raid member (1 to <code>MAX_RAID_MEMBERS</code>)
:;index2:{{apitype|number}} - ID of second raid member (1 to <code>MAX_RAID_MEMBERS</code>)

==Patch changes==
* {{Patch 4.0.1|note=Protected.}}

==See also==
* {{api|SetRaidSubgroup}}
```