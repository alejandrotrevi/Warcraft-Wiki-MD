# API UseAction

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the "action" type of the [[SecureActionButtonTemplate]].}}
Perform the action in the specified action slot.
 UseAction(slot [, checkCursor [, onSelf]])

==Arguments==
:;slot:{{apitype|number}} - The action [[ActionSlot|action slot]] to use.
:;checkCursor:{{apitype|number?}} - Can be 0, 1, or nil. Appears to indicate whether the action button was clicked (1) or used via hotkey (0); probably involved in placing skills/items in the action bar after they've been picked up.  I can confirm this.  If you pass 0 for checkCursor, it will use the action regardless of whether another item/skill is on the cursor.  If you pass 1 for checkCursor, it will replace the spell/action on the slot with the new one.
:;onSelf:{{apitype|number?}} - Can be 0, 1, or nil. If present and 1, then the action is performed on the player, not the target.  If "true" is passed instead of 1, Blizzard produces a Lua error.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}

==See also==
* {{api|GetActionInfo}}
```