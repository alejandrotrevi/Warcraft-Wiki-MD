# API GetSpellLossOfControlCooldown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a loss-of-control cooldown affecting a spell.
 start, duration = GetSpellLossOfControlCooldown(spellSlot[, bookType] or spellName or spellID)

==Arguments==
:;spellSlot:{{apitype|number}} - spell book slot index, ascending from 1.
:;bookType:{{apitype|string}} - spell book type token, e.g. "spell" from player's spell book.
or
:;spellName:{{apitype|string}} - name of a spell in the player's spell book.
or
:;spellID:{{apitype|number}} - spell ID of a spell accessible to the player.

==Returns==
:;start:{{apitype|number}} - time at which the loss-of-control cooldown began, per {{api|GetTime}}.
:;duration:{{apitype|number}} - duration of the loss-of-control cooldown in seconds; 0 if the spell is not currently affected by a loss-of-control cooldown.

==Details==
* If the spell is not affected by a loss-of-control cooldown, this function returns <code>0, 0</code>

==Patch changes==
* {{Patch 5.2.0|note=Added.}}

==See also==
* {{api|GetActionLossOfControlCooldown}}
```