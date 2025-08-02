# API GetRandomBGInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the current Call to Arms battleground.
 canQueue, battleGroundID, hasWon, winHonorAmount, winConquestAmount, lossHonorAmount, lossConquestAmount, minLevel, maxLevel = GetRandomBGInfo()

==Returns==
:;canQueue:{{apitype|boolean}} - true if the player can queue for a random battleground.
:;battleGroundID:{{apitype|number}} - random battleground queue map ID, 32.
:;hasWon:{{apitype|boolean}} - true if the the player has already won a random battleground once today, false otherwise.
:;winHonorAmount:{{apitype|number}} - amount of bonus Honor points awarded for winning.
:;winConquestAmount:{{apitype|number}} - amount of bonus Conquest points awarded for winning.
:;lossHonorAmount:{{apitype|number}} - amount of bonus Honor points awarded for losing.
:;lossConquestAmount:{{apitype|number}} - amount of bonus Conquest points awarded for losing.
:;minLevel:{{apitype|number}} - minimum character level at which random battlegrounds may be queued for.
:;maxLevel:{{apitype|number}} - maximum character level at which random battlegrounds may be queued for.

==Details==
* <code>battleGroundID</code> corresponds to a ''return value'' of {{api|GetBattlegroundInfo}}.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}

==See also==
* {{api|GetRandomBGHonorCurrencyBonuses}}
* {{api|RequestRandomBattlegroundInstanceInfo}}
```