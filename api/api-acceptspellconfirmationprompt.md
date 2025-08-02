# API AcceptSpellConfirmationPrompt

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Confirms a spell confirmation prompt (e.g. bonus loot roll).
 AcceptSpellConfirmationPrompt(spellID)

==Arguments==
:;spellID:{{apitype|number}} - spell ID of the prompt to confirm.

==Details==
* {{api|t=e|SPELL_CONFIRMATION_PROMPT}} fires when a spell confirmation prompt might be presented to the player; it provides the spellID and information about the type, text, and duration of the confirmation. Notably, the event does not guarantee that the player can actually cast the spell.
* Calling this function ''accepts'' the spell prompt, performing the action in question.
* {{api|t=e|SPELL_CONFIRMATION_TIMEOUT}} fires if the spell is not confirmed within the prompt duration.

==Patch changes==
* {{Patch 10.0.7|note=Protected.}}
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|DeclineSpellConfirmationPrompt}}
```