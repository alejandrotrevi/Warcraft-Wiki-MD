# API UnitAuraBySlot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}  {{deprecatedapi|patch=10.2.5|removed=11.0.2}}
Needs summary.
 name, icon, count, debuffType, duration, expirationTime, source, isStealable,
 nameplateShowPersonal, spellId, canApplyAura, isBossDebuff, castByPlayer, nameplateShowAll, timeMod, ... = UnitAuraBySlot(unit, slot)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]
:;slot:{{apitype|number}} - Aura slot from {{api|UnitAuraSlots}}()

==Returns==
{{:API_UnitAura}}

==Details==
<onlyinclude>It's recommended to just use [[API_UnitAura#ForEachAura|AuraUtil.ForEachAura]]() instead of <code>UnitAuraBySlot()</code> & <code>UnitAuraSlots()</code> as it'll "do the right thing".

<div class="darktable" style="margin: 1em auto; max-width: calc(50% + 48em); padding: 0.75em; font-size:100%">
'''2022-08-25 | Meorawr @ [https://discord.com/channels/168296152670797824/218957301111848962/1012454819782479974 Discord]'''

<div style="padding: 0.5em 0em;" class="text-blizz">With UnitAura the <code>index</code> parameter is a relative index into a list of auras specified by the <code>filter</code> parameter - so ''assuming zero optimizations'' each call effectively means that the client needs to traverse over the aura list each time counting how many auras match the given filter until the index is reached.

In reality it's likely got a basic optimization in-place that allows successive calls with the same unit/filter parameter to continue, thus bypassing that search.

UnitAuraSlots "advantage" is that it:
# Doesn't return just one aura slot.
# It returns a continuation token marking the number of slots the API can skip on the next call - basically making that above theoretical optimization explicit.</div>
</div></onlyinclude>

==Patch changes==
* {{Patch 10.2.5|note=Deprecated. Replaced by {{api|t=a|C_UnitAuras.GetAuraDataBySlot}}.}}
* {{Patch 8.2.5|note=Added.}}

{{apinavbox|UnitAura}}
```