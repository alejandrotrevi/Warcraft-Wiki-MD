# API GetSpellPowerCost

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns resource cost info for a spell.
 costs = GetSpellPowerCost(spell)
       = GetSpellPowerCost(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;costs:{{apitype|table[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| minCost || {{apitype|number}} || minimum cost
|-
| cost || {{apitype|number}} || maximum cost
|-
| costPercent || {{apitype|number}} || percentual cost
|-
| costPerSec || {{apitype|number}} || The cost per second for channeled spells.
|-
| type || {{apitype|Enum.PowerType}} || [[Enum.PowerType]]
|-
| name || {{apitype|string}} || powerToken: "MANA", "RAGE", "FOCUS", "ENERGY", "HAPPINESS", "RUNES", "RUNIC_POWER", "SOUL_SHARDS", "HOLY_POWER", "STAGGER", "CHI", "FURY", "PAIN", "LUNAR_POWER", "INSANITY"
|-
| hasRequiredAura || {{apitype|boolean}} || 
|-
| requiredAuraID || {{apitype|number}} || 
|}

==Details==
* Returns an empty table if the spell has no resource cost.
* Reflects resource discounts provided by auras.
* requiredAuraID has a return value different than zero for 36 spells. Most are spellIDs associated with a hidden healing/damage modifier spec aura, one refers to [[Bear Form]], two seem to be connected to [[Helya]]; some are honor talents, and some don't refer to a valid aura spellID. This return value mostly exists for spells that change their cost depending on which spec the player is in.
* Some spells may have costs composed of multiple resource types. In this case, the <code>costs</code> array contains multiple tables. For example, <code> GetSpellPowerCost("Rip")</code> returns
<div style="margin-left: 2em">
 {
   {type=3, name="ENERGY", cost=30, minCost=30, costPercent=0, costPerSec=0, hasRequiredAura=false, requiredAuraID=0},
   {type=4, name="COMBO_POINTS", cost=5, minCost=1, costPercent=0, costPerSec=0, hasRequiredAura=false, requiredAuraID=0}
 }
</div>
```