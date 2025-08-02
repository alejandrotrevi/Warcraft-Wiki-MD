# API DeclineSpellConfirmationPrompt

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Declines a spell confirmation prompt (e.g. bonus loot roll).
 DeclineSpellConfirmationPrompt(spellID)

==Arguments==
:;spellID:{{apitype|number}} - spell ID of the prompt to decline.

==Details==
* {{api|t=e|SPELL_CONFIRMATION_PROMPT}} fires when a spell confirmation prompt might be presented to the player; it provides the spellID and information about the type, text, and duration of the confirmation prompt.
* Calling this function ''declines'' the spell prompt: the player does ''not'' perform the prompted action.

==Patch changes==
* {{Patch 10.0.7|note=Protected.}}
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|AcceptSpellConfirmationPrompt}}
```