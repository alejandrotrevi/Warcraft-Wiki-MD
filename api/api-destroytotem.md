# API DestroyTotem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Destroys a totem/minion.
 DestroyTotem(slot)

==Arguments==
:;slot:{{apitype|number}} - The totem type to be destroyed, where Fire is 1, Earth is 2, Water is 3 and Air is 4.

==Triggers events==
* {{api|t=e|PLAYER_TOTEM_UPDATE}}
```