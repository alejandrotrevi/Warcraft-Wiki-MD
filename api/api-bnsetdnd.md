# API BNSetDND

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Sets the player's online DND status.
 BNSetDND(bool)

==Arguments==
:;bool:{{apitype|boolean}} - ''true'' set your battle.net status to dnd and ''false'' unset it.

==Details==
* [[API BNSetAFK|BNSetAFK]](true) can override dnd status
* [[API BNSetAFK|BNSetAFK]](false) can't unset dnd status
```