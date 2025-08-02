# API BNSetAFK

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Sets the player's online AFK status.
 BNSetAFK(bool)

==Arguments==
:;bool:{{apitype|boolean}} - ''true'' set your battle.net status to afk and ''false'' unset it.

==Details==
* [[API BNSetDND|BNSetDND]](true) can override afk status
* [[API BNSetDND|BNSetDND]](false) can't unset afk status
```