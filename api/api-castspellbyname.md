# API CastSpellByName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the "spell" action type of [[SecureActionButtonTemplate]] or the [[MACRO cast|/cast]] slash command.}}
Casts a spell by name.
 CastSpellByName(name [, target])

==Arguments==
:;name:{{apitype|string}} - Name of the spell to cast, e.g. "Alchemy".
:;target:{{apitype|string?}} : [[UnitId]] - The unit to cast the spell on. If omitted, "target" is assumed for spells that require a target.

==Details==
* You ''can'' still use this function to open trade skill windows and to summon mounts even from a tainted execution path.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```