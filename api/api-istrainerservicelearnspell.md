# API IsTrainerServiceLearnSpell

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the type of trainer spell in the trainer window.
 isLearnSpell, isPetLearnSpell = IsTrainerServiceLearnSpell(index)

==Arguments==
:;index:{{apitype|number}} - The index of the spell in the trainer window.

==Returns==
:;isLearnSpell:{{apitype|number}} - Returns 1 if the spell is a class spell or a learnable profession spell, nil otherwise.
:;isPetLearnSpell:{{apitype|number}} - Returns 1 if a pet spell, nil otherwise.

==Patch changes==
* {{Patch 2.4.0|note=Removed.}}

==See also==
* {{api|GetTrainerServiceInfo}}()
```