# API GetLFGRoleShortageRewards

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns info for the LFG [[Call_to_Arms_(dungeon)|Call to Arms]] rewards.
 eligible, forTank, forHealer, forDamage, itemCount, money, xp = GetLFGRoleShortageRewards(dungeonID, shortageSeverity)

==Arguments==
:;dungeonID:{{apitype|number}} : [[LfgDungeonID]] - The type of the dungeons to queue for. See table below.
:;shortageSeverity:{{apitype|number}} - A number from 1 to LFG_ROLE_NUM_SHORTAGE_TYPES. See below for specific shortage types.

==Returns==
:eligible, forTank, forHealer, forDamage, itemCount, money, xp  <!-- Include this line ONLY IF there are multiple return values and a large number of arguments -->
:;eligible:{{apitype|boolean}} - Unknown. Possibly whether there are any shortages of this type, possibly whether the player is somehow eligible to participate
:;forTank:{{apitype|boolean}} - Whether this shortage type applies to the tank role
:;forHealer:{{apitype|boolean}} - Whether this shortage type applies to the healer role
:;forDamage:{{apitype|boolean}} - Whether this shortage type applies to the damage role
:;itemCount:{{apitype|number}} - Unknown. Related to the potential rewards
:;money:{{apitype|number}} - Unknown. Most likely the amount of money you get as a reward
:;xp:{{apitype|number}} - Unknown. Most likely the amount of xp you get as a reward

==Dungeon IDs==
{| class="darktable zebra"
|-
! ID
! Type
|-
| 258 || Random Classic Dungeon
|-
| 259 || Random Burning Crusade Dungeon
|-
| 260 || Random Burning Crusade Heroic
|-
| 261 || Random Lich King Dungeon
|-
| 262 || Random Lich King Heroic
|-
| 300 || Random Cataclysm Dungeon
|-
| 301 || Random Cataclysm Heroic
|-
| 434 || Random Hour of Twilight Heroic
|-
| 462 || Random Mists of Pandaria Heroic
|-
| 463 || Random Mists of Pandaria Dungeon
|-
| 744 || Random Timewalking Dungeon
|-
| 788 || Random Warlords of Draenor Dungeon
|-
| 789 || Random Warlords of Draenor Heroic
|-
| 1045 || Random Legion Dungeon
|-
| 1046 || Random Legion Heroic
|-
| 1670 || Random Battle for Azeroth Dungeon
|-
| 1671 || Random Battle For Azeroth Heroic
|-
| 2086 || Random Shadowlands Dungeon
|-
| 2087 || Random Shadowlands Heroic
|}

The following snippet can be used to regenerate this list (for use with future patches):
 for i = 1, GetNumRandomDungeons() do
   local id, name = GetLFGRandomDungeonInfo(i)
   print(id .. ": " .. name)
 end

==Shortage Severities==
;LFG_ROLE_SHORTAGE_RARE - 1
;LFG_ROLE_SHORTAGE_UNCOMMON - 2
;LFG_ROLE_SHORTAGE_PLENTIFUL - 3
```