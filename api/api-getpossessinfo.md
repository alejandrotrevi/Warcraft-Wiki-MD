# API GetPossessInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an action on the possession bar.
 texture, spellID, enabled = GetPossessInfo(index)

==Arguments==
:;index:{{apitype|number}} - The slot of the possess bar to check, ascending from 1.

==Returns==
:;texture:{{apitype|string}} - The icon texture used for this slot, nil if the slot is empty
:;spellID:{{apitype|number}} - The name of the action in this slot, nil if the slot is empty.
:;enabled:{{apitype|boolean}} - true if there is an action in this slot, nil otherwise.

==Details==
* The possession bar is shown by the default UI (like a stance bar) while the player is controlling another target, such as while channeling [[Mind Control]].
* Typically, the first slot contains the spell used to control the other unit (which does nothing), while the second slot has a "Cancel" action that ends the effect.

==Patch changes==
* {{Patch 8.0.1|note=The second parameter was changed from spell name to spell ID. [https://us.battle.net/forums/en/wow/topic/20762318007]}}

==See also==
* {{api|IsPossessBarVisible}}
```