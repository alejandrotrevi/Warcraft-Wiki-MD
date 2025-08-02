# API FlyoutHasSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a flyout contains a specific spell.
 hasSpell = FlyoutHasSpell(flyoutID, spellID)

==Arguments==
:;flyoutID:{{apitype|number}} - flyout ID (as returned by {{api|GetSpellBookItemInfo}} or {{api|GetActionInfo}}).
:;spellID:{{apitype|number}} - spell ID.

==Returns==
:;hasSpell:{{apitype|boolean}} - true if the flyout contains the specified spell, false otherwise.

==Patch changes==
* {{Patch 5.1.0|note=Added.}}
```