# API GetQuestBackgroundMaterial

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the background texture for the displayed quest.

 material = GetQuestBackgroundMaterial()

==Returns==

:;material:{{apitype|string?}} - The material string for this quest, or nil if the default, "Parchment", is to be used.

==Details==
This texture is used to paint the background of the Blizzard Quest Frame. It does not appear in the Quest Log, but only when initially reading, accepting or handing in the quest.
```