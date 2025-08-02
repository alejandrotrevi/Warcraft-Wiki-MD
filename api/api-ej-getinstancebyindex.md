# API EJ GetInstanceByIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns instance info for the Encounter Journal.
 instanceID, name, description, bgImage, buttonImage1, loreImage, buttonImage2, dungeonAreaMapID, link, shouldDisplayDifficulty, mapID
     = EJ_GetInstanceByIndex(index, isRaid)

==Arguments==
:;index:{{apitype|number}}
:;isRaid:{{apitype|boolean}} - whether to return raid or normal instances.

==Returns==
:;1. instanceID:{{apitype|number}} : {{dbc|journalinstance|JournalInstance.ID}}
:;2. name:{{apitype|string}}
:;3. description:{{apitype|string}}
:;4. bgImage:{{apitype|number}} : [[FileID]]
:;5. buttonImage1:{{apitype|number}} : FileID
:;6. loreImage:{{apitype|number}} : FileID
:;7. buttonImage2:{{apitype|number}} : FileID
:;8. dungeonAreaMapID:{{apitype|number}} : [[UiMapID]] - 0 for raids before Siege of Orgrimmar (not including [[Timewalking]] raids), raid world bosses, and dungeons.
:;9. link:{{apitype|string}} : [[Hyperlinks#journal|journalLink]]
:;10. shouldDisplayDifficulty:{{apitype|boolean}}
:;11. mapID:{{apitype|number}} - The [[InstanceID]] for the instance.

==Gallery ==
<gallery>
API EJ GetInstanceByIndex 01.png
API EJ GetInstanceByIndex 02.png
API EJ GetInstanceByIndex 03.png
</gallery>

==Patch changes==
* {{Patch 4.2.0|note=Added.}}

==See also==
*{{api|EJ_GetInstanceInfo}}
```