# API SetRaidSubgroup

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 4.0.1}}
Move a raid member from his current subgroup into a different (non-full) subgroup.
 SetRaidSubgroup(index, subgroup)

==Arguments==
:;index:{{apitype|number}} - ID of raidmember (1 .. MAX_RAID_MEMBERS)
:;subgroup:{{apitype|number}} - raid subgroup number (1 .. 8)

==Example==
Move raid member with ID=25 into group 3
 SetRaidSubgroup(25, 3)
```