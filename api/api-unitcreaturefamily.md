# API UnitCreatureFamily

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the creature type of the unit (e.g. Crab).
 name, id = UnitCreatureFamily(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;name:{{apitype|string}} - localized name of the creature family (e.g., "Crab" or "Wolf").
:;id:{{apitype|number}} : {{dbc|CreatureFamily}}

==Details==
* Does not work on all creatures, since the family's primary function is to determine what abilities the unit will have if a player is able to control it. However, it does work on almost all Beasts, even if they are not tameable by Hunters.
* Returns nil if the creature doesn't belong to a family that includes a tameable creature.

==Example==
Displays a message if the target is a type of bear.
<syntaxhighlight lang="lua">
if select(2, UnitCreatureFamily("target")) == 4 then -- Bear
	print("It's a godless killing machine! Run for your lives!")
end
</syntaxhighlight>

==Values==
<!-- https://github.com/Ketho/WowpediaDoc/blob/master/Pages/UnitCreatureFamily.lua -->
<onlyinclude>{| class="vertical-align-row"
|
{| class="darktable zebra col1-center col2-center"
! ID !! Icon !! Name (enUS) !! Patch
|-
| 1 || [[File:ability_hunter_pet_wolf.png|24px|link=]] || Wolf || 
|-
| 2 || [[File:ability_hunter_pet_cat.png|24px|link=]] || Cat || 
|-
| 3 || [[File:ability_hunter_pet_spider.png|24px|link=]] || Spider || 
|-
| 4 || [[File:ability_hunter_pet_bear.png|24px|link=]] || Bear || 
|-
| 5 || [[File:ability_hunter_pet_boar.png|24px|link=]] || Boar || 
|-
| 6 || [[File:ability_hunter_pet_crocolisk.png|24px|link=]] || Crocolisk || 
|-
| 7 || [[File:ability_hunter_pet_vulture.png|24px|link=]] || Carrion Bird || 
|-
| 8 || [[File:ability_hunter_pet_crab.png|24px|link=]] || Crab || 
|-
| 9 || [[File:ability_hunter_pet_gorilla.png|24px|link=]] || Gorilla || 
|-
| 11 || [[File:ability_hunter_pet_raptor.png|24px|link=]] || Raptor || 
|-
| 12 || [[File:ability_hunter_pet_tallstrider.png|24px|link=]] || Tallstrider || 
|-
| 15 ||  || Felhunter || 
|-
| 16 ||  || Voidwalker || 
|-
| 17 ||  || Succubus || 
|-
| 19 ||  || Doomguard || 
|-
| 20 || [[File:ability_hunter_pet_scorpid.png|24px|link=]] || Scorpid || 
|-
| 21 || [[File:ability_hunter_pet_turtle.png|24px|link=]] || Turtle || 
|-
| 23 ||  || Imp || 
|-
| 24 || [[File:ability_hunter_pet_bat.png|24px|link=]] || Bat || 
|-
| 25 || [[File:ability_hunter_pet_hyena.png|24px|link=]] || Hyena || 
|-
| 26 || [[File:ability_hunter_pet_owl.png|24px|link=]] || Bird of Prey || 
|-
| 27 || [[File:ability_hunter_pet_windserpent.png|24px|link=]] || Wind Serpent || 
|-
| 28 ||  || Remote Control || 
|-
| 29 ||  || Felguard || 
|-
| 30 || [[File:ability_hunter_pet_dragonhawk.png|24px|link=]] || Dragonhawk || 
|-
| 31 || [[File:ability_hunter_pet_ravager.png|24px|link=]] || Ravager || 
|-
| 32 || [[File:ability_hunter_pet_warpstalker.png|24px|link=]] || Warp Stalker || 
|-
| 33 || [[File:ability_hunter_pet_sporebat.png|24px|link=]] || Sporebat || 
|-
| 34 || [[File:ability_hunter_pet_netherray.png|24px|link=]] || Ray || 
|-
| 35 || [[File:spell_nature_guardianward.png|24px|link=]] || Serpent || 
|-
| 37 || [[File:ability_hunter_pet_moth.png|24px|link=]] || Moth || 
|-
| 38 || [[File:ability_hunter_pet_chimera.png|24px|link=]] || Chimaera || 
|-
| 39 || [[File:ability_hunter_pet_devilsaur.png|24px|link=]] || Devilsaur || 
|-
| 40 || [[File:ability_creature_cursed_05.png|24px|link=]] || Ghoul || 
|-
| 41 || [[File:ability_hunter_pet_silithid.png|24px|link=]] || Aqiri || 
|-
| 42 || [[File:ability_hunter_pet_worm.png|24px|link=]] || Worm || 
|-
| 43 || [[File:inv_clefthoofdraenormount_blue.png|24px|link=]] || Clefthoof || 
|-
| 44 || [[File:ability_hunter_pet_wasp.png|24px|link=]] || Wasp || 
|-
| 45 || [[File:ability_hunter_pet_corehound.png|24px|link=]] || Core Hound || 
|-
| 46 || [[File:ability_druid_primalprecision.png|24px|link=]] || Spirit Beast || 
|-
| 49 ||  || Water Elemental || 
|-
| 50 || [[File:ability_hunter_aspectofthefox.png|24px|link=]] || Fox || 
|}
|
{| class="darktable zebra col1-center col2-center"
! ID !! Icon !! Name (enUS) !! Patch
|-
| 51 || [[File:inv_pet_monkey.png|24px|link=]] || Monkey || 
|-
| 52 || [[File:inv_pet_mastiff.png|24px|link=]] || Hound || 
|-
| 53 || [[File:inv_misc_ahnqirajtrinket_01.png|24px|link=]] || Beetle || 
|-
| 55 || [[File:inv_pet_ shalespider.png|24px|link=]] || Shale Beast || 
|-
| 56 || [[File:achievement_boss_patchwerk.png|24px|link=]] || Zombie || 
|-
| 57 || [[File:inv_scarab_stone.png|24px|link=]] || << QA TEST FAMILY >> || 
|-
| 68 || [[File:trade_archaeology_whitehydrafigurine.png|24px|link=]] || Hydra || 
|-
| 100 ||  || Fel Imp || 
|-
| 101 ||  || Voidlord || 
|-
| 102 ||  || Shivarra || 
|-
| 103 ||  || Observer || 
|-
| 104 ||  || Wrathguard || 
|-
| 108 ||  || Infernal || 
|-
| 116 || [[File:spell_fire_elemental_totem.png|24px|link=]] || Fire Elemental || 
|-
| 117 || [[File:spell_nature_earthelemental_totem.png|24px|link=]] || Earth Elemental || 
|-
| 125 || [[File:inv_pet_crane.png|24px|link=]] || Waterfowl || 
|-
| 126 || [[File:inv_pet_waterstrider.png|24px|link=]] || Water Strider || 
|-
| 127 || [[File:inv_pet_porcupine.png|24px|link=]] || Rodent || 
|-
| 128 || [[File:achievement_moguraid_01.png|24px|link=]] || Stone Hound || 
|-
| 129 || [[File:inv_pet_ goat.png|24px|link=]] || Gruffhorn || 
|-
| 130 || [[File:inv_pet_ basilisk.png|24px|link=]] || Basilisk || 
|-
| 138 || [[File:inv_pet_direhorn.png|24px|link=]] || Direhorn || 
|-
| 145 || [[File:ability_druid_galewinds.png|24px|link=]] || Storm Elemental || 
|-
| 147 ||  || Terrorguard || 
|-
| 148 ||  || Abyssal || 
|-
| 150 || [[File:inv_hippo_green.png|24px|link=]] || Riverbeast || 
|-
| 151 || [[File:inv_talbukdraenor_white.png|24px|link=]] || Stag || 
|-
| 154 || [[File:ability_mount_mechastrider.png|24px|link=]] || Mechanical || 
|-
| 155 || [[File:spell_shadow_abominationexplosion.png|24px|link=]] || Abomination || 
|-
| 156 || [[File:inv_mushanbeastmount.png|24px|link=]] || Scalehide || 
|-
| 157 || [[File:ability_mount_yakmount.png|24px|link=]] || Oxen || 
|-
| 160 || [[File:inv_misc_elitehippogryph.png|24px|link=]] || Feathermane || 
|-
| 288 || [[File:inv_komododragon_green.png|24px|link=]] || Lizard || 8.0.1
|-
| 290 || [[File:inv_pterrordax2mount_yellow.png|24px|link=]] || Pterrordax || 8.0.1
|-
| 291 || [[File:inv_pet_toad_green.png|24px|link=]] || Hopper || 8.0.1
|-
| 292 || [[File:achievement_dungeon_thesandqueen.png|24px|link=]] || Carapid || 8.0.1
|-
| 296 || [[File:inv_bloodtrollbeast_mount.png|24px|link=]] || Blood Beast || 8.1.0
|-
| 298 || [[File:ability_mount_camel_brown.png|24px|link=]] || Camel || 9.0.1
|-
| 299 || [[File:inv_horse3_pale.png|24px|link=]] || Courser || 9.0.1
|-
| 300 || [[File:ability_mount_ridingelekk.png|24px|link=]] || Mammoth || 9.0.1
|-
| 302 ||  || Incubus || 9.2.0
|-
| 303 || [[File:inv_misc_head_dragon_nexus.png|24px|link=]] || Lesser Dragonkin || 10.0.0
|}
|}</onlyinclude>

==Patch changes==
* {{Patch 11.1.5|note=Added <code>id</code> return value. [https://github.com/Stanzilla/WoWUIBugs/issues/118 WoWUIBugs#118]}}
```