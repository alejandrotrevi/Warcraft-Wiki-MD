# API GetHolidayBGInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the current Call to Arms battleground.
 canQueue, bgName, battleGroundID, hasWon, winHonorAmount, winConquestAmount, lossHonorAmount, lossConquestAmount, minLevel, maxLevel = GetHolidayBGInfo()

==Returns==
:;canQueue:{{apitype|boolean}} - true if the player can queue for this battleground.
:;bgName:{{apitype|string}} - name of the battleground currently awarding bonus rewards, e.g. "Strand of the Ancients"
:;battleGroundID:{{apitype|number}} - battleground map ID of the battleground currently awarding bonus rewards, e.g. 9 for Strand of the Ancients.
:;hasWon:{{apitype|boolean}} - true if the the player has already won the battleground once today, false otherwise.
:;winHonorAmount:{{apitype|number}} - amount of bonus Honor points awarded for winning.
:;winConquestAmount:{{apitype|number}} - amount of bonus Conquest points awarded for winning.
:;lossHonorAmount:{{apitype|number}} - amount of bonus Honor points awarded for losing.
:;lossConquestAmount:{{apitype|number}} - amount of bonus Conquest points awarded for losing.
:;minLevel:{{apitype|number}} - minimum character level at which this battleground may be queued for.
:;maxLevel:{{apitype|number}} - maximum character level at which this battleground may be queued for.

==Details==
* <code>battleGroundID</code> corresponds to a ''return value'' of {{api|GetBattlegroundInfo}}.

==Patch changes==
* {{Patch 5.4.7|note=New 'hasData' return value added to ''beginning'' of list.}}
* {{Patch 5.2.0|note=Added.}}

==See also==
* {{api|GetHolidayBGHonorCurrencyBonuses}}
```