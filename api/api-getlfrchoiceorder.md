# API GetLFRChoiceOrder

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Seems to be for used ordering the LFR list.
 raidList = GetLFRChoiceOrder([LFRRaidList])

==Arguments==
:;LFRRaidList:{{apitype|table}} - ?

==Returns==
:;raidList:{{apitype|table}} - Key = ?; Value = Dungeon ID

==Example==
 /run for i, v in ipairs(GetLFRChoiceOrder()) do print(i, v, GetLFGDungeonInfo(v)) end

<pre>
1, -33, "Hour of Twilight Heroic", 1
2, -12, "Cataclysm Heroic", 1
3, -13, "Cataclysm Normal", 1
4, -5, "Wrath of the Lich King Heroic", 1
5, -4, "Wrath of the Lich King Normal", 1
6, -3, "Burning Crusade Heroic", 1
7, -2, "Burning Crusade Normal", 1
8, -1, "Classic Dungeons", 1
9, -14, "Cataclysm Raid (25)", 2
10, 329, "Baradin Hold", 2, 0, 85, 85, 85, 85, 85, 3, -14, "BARADINHOLD", 1, 25, "", false
11, 314, "Blackwing Descent", 2, 0, 85, 85, 85, 85, 85, 3, -14, "BLACKWINGDESCENTRAID", 1, 25, "", false
12, 448, "Dragon Soul", 2, 0, 85, 85, 85, 85, 85, 3, -14, "DRAGONSOUL", 1, 25, "", false
13, 362, "Firelands", 2, 0, 85, 85, 85, 85, 85, 3, -14, "FIRELANDS", 1, 25, "", false
14, 316, "The Bastion of Twilight", 2, 0, 85, 85, 85, 85, 85, 3, -14, "GRIMBATOLRAID", 1, 25, "", false
15, 318, "Throne of the Four Winds", 2, 0, 85, 85, 85, 85, 85, 3, -14, "THRONEOFTHEFOURWINDS", 1, 25, "", false
16, -15, "Cataclysm Raid (10)", 2
17, 328, "Baradin Hold", 2, 0, 85, 85, 85, 85, 85, 3, -15, "BARADINHOLD", 0, 10, "", false
18, 313, "Blackwing Descent", 2, 0, 85, 85, 85, 85, 85, 3, -15, "BLACKWINGDESCENTRAID", 0, 10, "", false
19, 447, "Dragon Soul", 2, 0, 85, 85, 85, 85, 85, 3, -15, "DRAGONSOUL", 0, 10, "", false
20, 361, "Firelands", 2, 0, 85, 85, 85, 85, 85, 3, -15, "FIRELANDS", 0, 10, "", false
21, 315, "The Bastion of Twilight", 2, 0, 85, 85, 85, 85, 85, 3, -15, "GRIMBATOLRAID", 0, 10, "", false
22, 317, "Throne of the Four Winds", 2, 0, 85, 85, 85, 85, 85, 3, -15, "THRONEOFTHEFOURWINDS", 0, 10, "", false
23, -9, "Wrath of the Lich King Raid (25)", 2
24, 280, "Icecrown Citadel", 2, 0, 80, 83, 80, 80, 83, 2, -9, "ICECROWNCITADEL", 1, 25, "", false
25, 227, "Naxxramas", 2, 0, 80, 83, 80, 80, 83, 2, -9, "NAXXRAMAS", 1, 25, "", false
26, 257, "Onyxia's Lair", 2, 0, 80, 83, 80, 80, 83, 2, -9, "ONYXIAENCOUNTER", 1, 25, "", false
27, 294, "Ruby Sanctum", 2, 0, 80, 83, 80, 80, 83, 2, -9, "RUBYSANCTUM", 1, 25, "", false
28, 237, "The Eye of Eternity", 2, 0, 80, 83, 80, 80, 83, 2, -9, "MALYGOS", 1, 25, "", false
29, 238, "The Obsidian Sanctum", 2, 0, 80, 83, 80, 80, 83, 2, -9, "CHAMBEROFASPECTS", 1, 25, "", false
30, 248, "Trial of the Crusader", 2, 0, 80, 83, 80, 80, 83, 2, -9, "ARGENTRAID", 1, 25, "", false
31, 250, "Trial of the Grand Crusader", 2, 0, 80, 83, 80, 80, 83, 2, -9, "ARGENTRAID", 3, 25, "", false
32, 244, "Ulduar", 2, 0, 80, 83, 80, 80, 83, 2, -9, "ULDUAR", 1, 25, "", false
33, 240, "Vault of Archavon", 2, 0, 80, 83, 80, 80, 83, 2, -9, "VAULTOFARCHAVON", 1, 25, "", false
34, -8, "Wrath of the Lich King Raid (10)", 2
35, 279, "Icecrown Citadel", 2, 0, 80, 83, 80, 80, 83, 2, -8, "ICECROWNCITADEL", 0, 10, "", false
36, 159, "Naxxramas", 2, 0, 80, 83, 80, 80, 83, 2, -8, "NAXXRAMAS", 0, 10, "", false
37, 46, "Onyxia's Lair", 2, 0, 80, 83, 80, 80, 83, 2, -8, "ONYXIAENCOUNTER", 0, 10, "", false
38, 293, "Ruby Sanctum", 2, 0, 80, 83, 80, 80, 83, 2, -8, "RUBYSANCTUM", 0, 10, "", false
39, 223, "The Eye of Eternity", 2, 0, 80, 83, 80, 80, 83, 2, -8, "MALYGOS", 0, 10, "", false
40, 224, "The Obsidian Sanctum", 2, 0, 80, 83, 80, 80, 83, 2, -8, "CHAMBEROFASPECTS", 0, 10, "", false
41, 246, "Trial of the Crusader", 2, 0, 80, 83, 80, 80, 83, 2, -8, "ARGENTRAID", 0, 10, "", false
42, 247, "Trial of the Grand Crusader", 2, 0, 80, 83, 80, 80, 83, 2, -8, "ARGENTRAID", 2, 10, "", false
43, 243, "Ulduar", 2, 0, 80, 83, 80, 80, 83, 2, -8, "ULDUAR", 0, 10, "", false
44, 239, "Vault of Archavon", 2, 0, 80, 83, 80, 80, 83, 2, -8, "VAULTOFARCHAVON", 0, 10, "", false
45, -7, "Burning Crusade Raid", 2
46, 196, "Black Temple", 2, 0, 70, 70, 70, 70, 70, 1, -7, "BLACKTEMPLE", 0, 25, "", false
47, 177, "Gruul's Lair", 2, 0, 70, 70, 70, 70, 70, 1, -7, "GRUULSLAIR", 0, 25, "", false
48, 195, "Hyjal Past", 2, 0, 70, 70, 70, 70, 70, 1, -7, "HYJALPAST", 0, 25, "", false
49, 175, "Karazhan", 2, 0, 70, 70, 70, 70, 70, 1, -7, "KARAZHAN", 0, 10, "", false
50, 176, "Magtheridon's Lair", 2, 0, 70, 70, 70, 70, 70, 1, -7, "HELLFIRECITADELRAID", 0, 25, "", false
51, 194, "Serpentshrine Cavern", 2, 0, 70, 70, 70, 70, 70, 1, -7, "SERPENTSHRINECAVERN", 0, 25, "", false
52, 193, "Tempest Keep", 2, 0, 70, 70, 70, 70, 70, 1, -7, "TEMPESTKEEP", 0, 25, "", false
53, 199, "The Sunwell", 2, 0, 70, 70, 70, 70, 70, 1, -7, "SUNWELL", 0, 25, "", false
54, -6, "Classic Raid", 2
55, 160, "Ahn'Qiraj Ruins", 2, 0, 60, 60, 60, 60, 60, 0, -6, "AQRUINS", 0, 10, "", false
56, 161, "Ahn'Qiraj Temple", 2, 0, 60, 60, 60, 60, 60, 0, -6, "AQTEMPLE", 0, 40, "", false
57, 50, "Blackwing Lair", 2, 0, 60, 60, 60, 60, 60, 0, -6, "BLACKWINGLAIR", 0, 40, "", false
58, 48, "Molten Core", 2, 0, 60, 60, 60, 60, 60, 0, -6, "MOLTENCORE", 0, 40, "", false
59, -11, "World Events", 0
60, -20, "Rated Battleground", 2
61, 358, "10v10 Rated Battleground", 2, 0, 85, 85, 85, 85, 85, 3, -20, "WARSONGGULCH", 0, 0, "", false
</pre>
```