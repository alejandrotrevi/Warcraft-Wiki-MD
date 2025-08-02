# API C PartyInfo.LeaveParty

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Leaves the group.
 C_PartyInfo.LeaveParty([category])

==Arguments==
:;category:{{apitype|number?}}
{{:LE_PARTY_CATEGORY|nocaption=1}}

==Details==
* Usually this will leave the party immediately. In some cases (e.g. PartySync) the user will be prompted to confirm leaving the party, because it's potentially destructive

==Patch changes==
* {{Patch 8.2.5|note=Moved to <code>C_PartyInfo.LeaveParty()</code>}}
* {{Patch 1.0.0|note=Added as {{api|LeaveParty}}()}}
```