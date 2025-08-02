# API GetLootRollItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__

Returns information about the loot event with rollID.

 texture, name, count, quality, bindOnPickUp, canNeed, canGreed, canDisenchant, reasonNeed, reasonGreed, reasonDisenchant, deSkillRequired, canTransmog = GetLootRollItemInfo(rollID)

==Arguments==
:;rollID:{{apitype|number}} - The number increments by 1 for each new roll. The count is not reset by reloading the UI.

==Returns==

:;texture:{{apitype|string}} - The path of the texture of the item icon.
:;name:{{apitype|string}} - The name of the item.
:;count:{{apitype|number}} - The quantity of the item.
:;quality:{{apitype|number}} - The [[quality]] of the item. Starting with 1 for [[common (quality)|common]], going up to 5 for [[legendary]].
:;bindOnPickUp:{{apitype|boolean}} - Returns 1 when the item is [[bind on pickup]], nil otherwise.
:;canNeed:{{apitype|boolean}} - Returns 1 when you can roll [[need]] on the item, nil otherwise.
:;canGreed:{{apitype|boolean}} - Returns 1 when you can roll [[greed]] on the item, nil otherwise.
:;canDisenchant:{{apitype|boolean}} - Returns 1 when you can [[disenchant]] the item, nil otherwise.
:;reasonNeed:{{apitype|number}} - See details.
:;reasonGreed:{{apitype|number}} - See details.
:;reasonDisenchant:{{apitype|number}} - See details.
:;deSkillRequired:{{apitype|number}} - Required skill in [[enchanting]] to disenchant the item.
:;canTransmog:{{apitype|boolean}} - Returns 1 when you can [[transmogrify]] the item, nil otherwise.

==Details==

The return values reasonNeed/reasonGreed/reasonDisenchant can be numbers from 0 to 5. The following logic is used in [[FrameXML]]:

If the player cannot roll need/greed/disenchant, the respective loot button is disabled and gets a tooltip from one of the following global strings, where the number is determined by the return values reasonNeed/reasonGreed/reasonDisenchant:

* LOOT_ROLL_INELIGIBLE_REASON1: "Your class may not roll need on this item."
* LOOT_ROLL_INELIGIBLE_REASON2: "You already have the maximum amount of this item."
* LOOT_ROLL_INELIGIBLE_REASON3: "This item may not be disenchanted."
* LOOT_ROLL_INELIGIBLE_REASON4: "You do not have an Enchanter of skill %d in your group."
* LOOT_ROLL_INELIGIBLE_REASON5: "Need rolls are disabled for this item."
* LOOT_ROLL_INELIGIBLE_REASON6: "You already have a powerful version of this item."
* LOOT_ROLL_INELIGIBLE_REASON7: "You do not have the profession required to use this item."

For example ''NeedButton.reason = _G["LOOT_ROLL_INELIGIBLE_REASON"..reasonNeed]''. If the player ''can'' roll need/greed/disenchant the respective value of reasonNeed/reasonGreed/reasonDisenchant returns 0.

==Patch changes==
* {{Patch 1.11|note=Added ''bindOnPickUp'' return.}}
```