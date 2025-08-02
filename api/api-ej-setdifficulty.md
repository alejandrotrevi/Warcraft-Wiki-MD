# API EJ SetDifficulty

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the encounter difficulty shown in the Encounter Journal.
 EJ_SetDifficulty(difficultyID)

==Arguments==
:;[[DifficultyID|difficultyID]]:{{apitype|number}} - ID of the difficulty to display ability/loot/encounter information for, as per {{api|GetDifficultyInfo}}.

==Triggers events==
* {{api|t=e|EJ_DIFFICULTY_UPDATE}}

==Patch changes==
* {{Patch 5.4.0|note=This function now uses standard instance difficulty IDs rather than its own enumeration.}}
* {{Patch 4.2.0|note=Added.}}
```