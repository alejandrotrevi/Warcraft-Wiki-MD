# API CanDualWield

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the player can [[Dual wield]] weapons.
 canDualWield = CanDualWield()

==Returns==
:;canDualWield:{{apitype|boolean}} - This returns true if One-Hand weapons can be equipped into both INVSLOT_MAINHAND and INVSLOT_OFFHAND.

==Details==
* Fury Warriors can dual wield one-hand weapons, and two-hand weapons (or a combination) from the baseline [[Titan's Grip]] passive.

==Values==
====<font color="#4ec9b0">Retail</font>====
{| class="sortable darktable zebra"
|-
! Class !! CanDualWield !! IsSpellKnown !! IsPlayerSpell
|-
| {{ClassIcon|Rogue}} Rogue<br>{{ClassIcon|Hunter}} Hunter<br>{{ClassIcon|Demon Hunter}} Demon Hunter<br>{{ClassIcon|Death Knight}} Frost Death Knight || align="center" | ✔️ || ❌ [https://www.wowhead.com/spell=674/dual-wield 674] || ✔️ 674
|-
| {{ClassIcon|Monk}} Brewmaster Monk<br>{{ClassIcon|Monk}} Windwalker Monk<br>{{ClassIcon|Shaman}} Enhancement Shaman || align="center" | ✔️ || ❌ 674 || ❌ 674
|-
| {{ClassIcon|Warrior}} Fury Warrior || align="center" | ✔️ || ❌ 674, ✔️ [https://www.wowhead.com/spell=46917/titans-grip 46917] || ❌ 674, ✔️ 46917
|}

====<font color="#4ec9b0">Classic</font>====
{| class="sortable darktable zebra"
|-
! Class !! CanDualWield !! IsSpellKnown !! IsPlayerSpell
|-
| {{ClassIcon|Rogue}} Rogue (level 10)<br>{{ClassIcon|Hunter}} Hunter (level 20)<br>{{ClassIcon|Warrior}} Warrior (level 20)|| align="center" | ✔️ || ✔️ 674 || ✔️ 674
|}

==See also==
* [[Enum.InventoryType]]
* [[InventorySlotId]]
```