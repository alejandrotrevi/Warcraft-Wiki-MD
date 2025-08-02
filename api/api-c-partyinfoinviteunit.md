# API C PartyInfo.InviteUnit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Invites a player to your group.
 C_PartyInfo.InviteUnit(name)

==Arguments==
:;name:{{apitype|string}} - The name of the player you would like to invite.

==Details==
* Attempt to invite the named unit to a party, requires confirmation in some cases (e.g. the party will convert to a raid, or if there is a party sync in progress).

==Patch changes==
* {{Patch 8.2.5|note=Moved to <code>C_PartyInfo.InviteUnit()</code>. The previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.2.5/Blizzard_Deprecated/Deprecated_8_2_5.lua#369]. Replaces the [https://www.townlong-yak.com/framexml/8.2.0/UIParent.lua#4247 InviteToGroup]() FrameXML function.}}
* {{Patch 3.0.8|note=No longer accepts [[UnitId]]s, use the player name instead.}}
* {{Patch 2.0.1|note=Moved to <code>InviteUnit()</code>}}
* {{Patch 1.0.0|note=Added as <code>InviteByName()</code>}}
```