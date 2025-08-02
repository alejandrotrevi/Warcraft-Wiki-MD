# API EJ GetInstanceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns instance info for the Encounter Journal.
 name, description, bgImage, buttonImage1, loreImage, buttonImage2, dungeonAreaMapID, link, shouldDisplayDifficulty, mapID
     = EJ_GetInstanceInfo([journalInstanceID])

==Arguments==
:;journalInstanceID:{{apitype|number?}} : [https://wago.tools/db2/JournalInstance JournalInstance.ID] - If omitted, defaults to the currently selected instance from {{api|EJ_SelectInstance}}()

==Returns==
:;1. name:{{apitype|string}}
:;2. description:{{apitype|string}}
:;3. bgImage:{{apitype|number}} : [[FileID]]
:;4. buttonImage1:{{apitype|number}} : FileID
:;5. loreImage:{{apitype|number}} : FileID
:;6. buttonImage2:{{apitype|number}} : FileID
:;7. dungeonAreaMapID:{{apitype|number}} : [[UiMapID]] - 0 for raids before Siege of Orgrimmar (not including [[Timewalking]] raids), raid world bosses, and dungeons.
:;8. link:{{apitype|string}} : [[Hyperlinks#journal|journalLink]]
:;9. shouldDisplayDifficulty:{{apitype|boolean}}
:;10. mapID:{{apitype|number}} - The [[InstanceID]] for the instance.

==Patch changes==
* {{Patch 4.2.0|note=Added.}}

==See also==
* {{api|EJ_GetInstanceByIndex}}
```