# API InviteUnit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Invite a player to join your party.
 InviteUnit(playerName)

==Arguments==
:;playerName:{{apitype|string}} - The name of the player you would like to invite to a group. 

==Details==
* Do not prehook this function in Classic Wrath as the LFG/Group Finder uses it directly. Only Secure Hook it. 

==Patch changes==
* {{Patch 3.0.8|note=This function originally accepted [[unitId]]s as a possible argument, but was changed in the patch to accept only player names.|comment=Code should be updated to use [[API UnitName|UnitName]]("unit") instead.}}
* {{Patch 2.0.1|note=Added, replacing <code>InviteByName</code>.}}

==See also==
* {{api|UninviteUnit}}
* {{api|InviteToGroup}}
```