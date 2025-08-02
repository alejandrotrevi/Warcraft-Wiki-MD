# API SpellStopCasting

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the [[stopcasting|/stopcasting]] slash command.}}
Stops the current spellcast.
 stopped = SpellStopCasting()

==Returns==
:;stopped:{{apitype|boolean}} - 1 if a spell was being cast, nil otherwise.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```