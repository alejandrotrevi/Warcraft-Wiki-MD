# API GetInventoryAlertStatus

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the durability status of an equipped item.
 alertStatus = GetInventoryAlertStatus(index)

==Arguments==
:;index:{{apitype|string}} - one of the following:
:* Head
:* Shoulders
:* Chest
:* Waist
:* Legs
:* Feet
:* Wrists
:* Hands
:* Weapon
:* Shield
:* Ranged

==Returns==
:;alertStatus:{{apitype|number}} - 0 for normal (6 or more durability points left), 1 for yellow (5 to 1 durability points left), 2 for broken (0 durability points left).

==Details==
* Used primarily for DurabilityFrame, ie the armor man placed under the Minimap when your equipment is damaged or broken.
```