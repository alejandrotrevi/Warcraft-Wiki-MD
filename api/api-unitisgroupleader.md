# API UnitIsGroupLeader

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns whether the unit is the leader of a party or raid.
 isLeader = UnitIsGroupLeader(unit [, partyCategory])

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]
:;partyCategory:{{apitype|number?}}
{{:LE_PARTY_CATEGORY|nocaption=1}}

==Returns==
:;isLeader:{{apitype|boolean}}

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```