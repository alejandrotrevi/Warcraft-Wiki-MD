# API GetNumBattlefieldStats

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Appears to return the number of columns in the battleground/field scoreboard, other than the common ones (Killing Blows, Kills, Deaths, Bonus Honour):

 local numStats = GetNumBattlefieldStats()

==Parameters==
===Returns===

:;numStats:{{apitype|number}} - Number of columns available for the battleground (2 for [[Warsong Gulch]] and [[Arathi Basin]], 7 for [[Alterac Valley]])
```