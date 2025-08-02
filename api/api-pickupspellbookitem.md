# API PickupSpellBookItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 4.0.1; Fails silently if called from insecure code in combat.}}
Picks up a skill from spellbook so that it can subsequently be placed on an action bar.
 PickupSpellBookItem(spell)
 PickupSpellBookItem(index, bookType)
==Arguments==
{{:SpellArg}}

==Example==
The following sequence of macro commands places the Cat Form ability into the current action bar's first slot.
 /run PickupSpellBookItem("Cat Form")
 /click ActionButton1
 /run ClearCursor()

==Patch changes==
* {{Patch 4.0.1|note=Added. Replaces some {{api|PickupSpell}}() functionality.}}
```