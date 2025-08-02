# API GetQuestDifficultyColor

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__


Gets the difficulty colour for a given level compared to the player's level.
 colour = GetQuestDifficultyColor(level)


==Arguments==
:;level:{{apitype|number}} - The level to be compared to the player's current level.


==Returns==
:;colour:Table - A table containing the RGB value of the resulting colour.
:;;*"r" - The red channel of the colour. Ranging from 0.0 to 1.0
:;;*"g" - The green channel of the colour. Ranging from 0.0 to 1.0
:;;*"b" - The blue channel of the colour. Ranging from 0.0 to 1.0


==Example==
 local colour = GetQuestDifficultyColor(47);
 DEFAULT_CHAT_FRAME:AddMessage("Your difficulty colour against a target of level 47.", colour.r, colour.g, colour.b);

==Details==
: Changed from GetDifficultyColor to GetQuestDifficultyColor in Patch 3.2
```