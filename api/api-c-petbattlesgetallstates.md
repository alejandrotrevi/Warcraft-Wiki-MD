# API C PetBattles.GetAllStates

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns all state IDs.
 stateIDs = C_PetBattles.GetAllStates([stateEnv])

==Arguments==
:;stateEnv:{{apitype|table?}} - If supplied, this table will be filled with all known state IDs.

==Returns==
:;stateIDs:{{apitype|table<string,number>}} - A table with all state IDs. If <code>stateEnv</code> is supplied, the returned table will be the same table .

==Details==
This function is typically used so that the developer can correlate state IDs (numbers like 125) to state names (strings like "STATE_BIGGLESWORTH_WHISKERS") and/or to use the state IDs in one of the two functions that require them as an argument.

==Current Values==
These are the current stateIDs as of [[Patch 11.0.2]]. More may be added to the end of this list in future patches, but it is unlikely any will be removed (based on the large amount of unused stateIDs currently in the below table).
<syntaxhighlight lang="lua">
1: STATE_Is_Dead
2: STATE_maxHealthBonus
3: STATE_Internal_InitialHealth
4: STATE_Stat_Kharma
17: STATE_Internal_InitialLevel
18: STATE_Stat_Power
19: STATE_Stat_Stamina
20: STATE_Stat_Speed
21: STATE_Mechanic_IsPoisoned
22: STATE_Mechanic_IsStunned
23: STATE_Mod_DamageDealtPercent
24: STATE_Mod_DamageTakenPercent
25: STATE_Mod_SpeedPercent
26: STATE_Ramping_DamageID
27: STATE_Ramping_DamageUses
28: STATE_Condition_WasDamagedThisTurn
29: STATE_untargettable
30: STATE_Mechanic_IsUnderground
31: STATE_Last_HitTaken
32: STATE_Last_HitDealt
33: STATE_Mechanic_IsFlying
34: STATE_Mechanic_IsBurning
35: STATE_turnLock
36: STATE_swapOutLock
40: STATE_Stat_CritChance
41: STATE_Stat_Accuracy
42: STATE_Passive_Critter
43: STATE_Passive_Beast
44: STATE_Passive_Humanoid
45: STATE_Passive_Flying
46: STATE_Passive_Dragon
47: STATE_Passive_Elemental
48: STATE_Passive_Mechanical
49: STATE_Passive_Magic
50: STATE_Passive_Undead
51: STATE_Passive_Aquatic
52: STATE_Mechanic_IsChilled
53: STATE_Weather_BurntEarth
54: STATE_Weather_ArcaneStorm
55: STATE_Weather_Moonlight
56: STATE_Weather_Darkness
57: STATE_Weather_Sandstorm
58: STATE_Weather_Blizzard
59: STATE_Weather_Mud
60: STATE_Weather_Rain
61: STATE_Weather_Sunlight
62: STATE_Weather_LightningStorm
63: STATE_Weather_Windy
64: STATE_Mechanic_IsWebbed
65: STATE_Mod_HealingDealtPercent
66: STATE_Mod_HealingTakenPercent
67: STATE_Mechanic_IsInvisible
68: STATE_unkillable
69: STATE_Mechanic_IsObject
70: STATE_Special_Plant
71: STATE_Add_FlatDamageTaken
72: STATE_Add_FlatDamageDealt
73: STATE_Stat_Dodge
74: STATE_Special_BlockedAttackCount
75: STATE_Special_ObjectRedirectionAuraID
77: STATE_Mechanic_IsBleeding
78: STATE_Stat_Gender
82: STATE_Mechanic_IsBlind
84: STATE_Cosmetic_Stealthed
85: STATE_Cosmetic_WaterBubbled
87: STATE_Mod_PetTypeDamageDealtPercent
88: STATE_Mod_PetTypeDamageTakenPercent
89: STATE_Mod_PetType_ID
90: STATE_Internal_CaptureBoost
91: STATE_Internal_EffectSucceeded
93: STATE_Special_IsCockroach
98: STATE_swapInLock
99: STATE_Mod_MaxHealthPercent
100: STATE_Clone_Active
101: STATE_Clone_PBOID
102: STATE_Clone_PetAbility1
103: STATE_Clone_PetAbility2
104: STATE_Clone_PetAbility3
105: STATE_Clone_Health
106: STATE_Clone_MaxHealth
107: STATE_Clone_LastAbilityID
108: STATE_Clone_LastAbilityTurn
113: STATE_Special_IsCharging
114: STATE_Special_IsRecovering
117: STATE_Clone_CloneAbilityID
118: STATE_Clone_CloneAuraID
119: STATE_DarkSimulacrum_AbilityID
120: STATE_Special_ConsumedCorpse
121: STATE_Ramping_PBOID
122: STATE_reflecting
123: STATE_Special_BlockedFriendlyMode
124: STATE_Special_TypeOverride
126: STATE_Mechanic_IsWall
127: STATE_Condition_DidDamageThisRound
128: STATE_Cosmetic_FlyTier
129: STATE_Cosmetic_FetishMask
136: STATE_Mechanic_IsBomb
141: STATE_Special_IsCleansing
144: STATE_Cosmetic_Bigglesworth
145: STATE_Internal_HealthBeforeInstakill
149: STATE_resilient
153: STATE_Passive_Elite
158: STATE_Cosmetic_Chaos
162: STATE_Passive_Boss
176: STATE_Cosmetic_TreasureGoblin
191: STATE_Ignore_Damage_Below_Threshold
196: STATE_Cosmetic_Spectral_Blue
199: STATE_Special_Egg
200: STATE_Ignore_Damage_Above_Threshold
201: STATE_Cheating_Death
202: STATE_Add_PeriodicDamageTaken
302: STATE_Dealt_KillingBlow
303: STATE_Passive_Leprosy
304: STATE_Special_Auto_Rebuilder
305: STATE_Special_Necrotic_Touch
306: STATE_Special_Redirect_Healing
313: STATE_Special_Intercept_Damage
314: STATE_Critical_Damage_Bonus
315: STATE_Internal_Never_Cancel_Spell_Visual
316: STATE_Weather_Toxic_Gas
319: STATE_Internal_Immune_Knockback
320: STATE_Special_Stored_Up_Damage
321: STATE_Special_IsFromZM
</syntaxhighlight>

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.GetAbilityStateModification}}
* {{api|C_PetBattles.GetStateValue}}
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]

<!-- luals
---@param stateEnv? table
---@return table<string, number> stateIDs
function C_PetBattles.GetAllStates(stateEnv) end
-->
```