# API C MountJournal.GetMountInfoExtraByID

**Contributor:** Eithris

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns extra information about the specified mount.
 creatureDisplayInfoID, description, source, isSelfMount, mountTypeID,
 uiModelSceneID, animID, spellVisualKitID, disablePlayerMountPreview
     = C_MountJournal.GetMountInfoExtraByID(mountID)
     = C_MountJournal.GetDisplayedMountInfoExtra(index)

==Arguments==
===<font color="#4ec9b0">GetMountInfoExtraByID</font>===
:;mountID:{{apitype|number}} : [[MountID]] - Returned from {{api|C_MountJournal.GetMountIDs}}()

===<font color="#4ec9b0">GetDisplayedMountInfoExtra</font>===
:;displayIndex:{{apitype|number}} - Index of the displayed mount in the mount journal list with the current search query and filters. Ranging from 1 to {{api|C_MountJournal.GetNumDisplayedMounts}}()

==Returns==
:;creatureDisplayInfoID:{{apitype|number}} : [[DisplayID]] - If <code>nil</code>, then the mount has multiple displayIDs, from {{api|C_MountJournal.GetMountAllCreatureDisplayInfoByID}}()<sup>[https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Collections/Blizzard_MountCollection.lua#206]</sup>. This is not consistent however, since this can be not nil and still have multiple displayIds.
:;description:{{apitype|string}} - flavor text describing the mount
:;source:{{apitype|string}} - information about how the mount is obtained, including vendor name and location, monetary cost, etc.
:;isSelfMount:{{apitype|boolean}} - true if the player transforms into the mount (eg. [[Obsidian Nightwing]] or [[Sandstone Drake]]), or false for normal mounts
:;mountTypeID:{{apitype|number}} - a number indicating the capabilities of the mount; known values include:
::* 230 for most ground mounts
::* 231 for [[Riding Turtle]] and [[Sea Turtle]]
::* 232 for [[Vashj'ir Seahorse]] (was named [[Abyssal Seahorse]] prior to [[Warlords of Draenor]])
::* 241 for [[Blue Qiraji Battle Tank|Blue]], [[Green Qiraji Battle Tank|Green]], [[Red Qiraji Battle Tank|Red]], and [[Yellow Qiraji Battle Tank]] (restricted to use inside [[Temple of Ahn'Qiraj]])
::* 242 for [[Swift Spectral Gryphon]] (hidden in the mount journal, used while dead in certain zones)
::* 247 for [[Disc of the Red Flying Cloud]]
::* 248 for most flying mounts, including those that change capability based on riding skill
::* 254 for [[Reins of Poseidus]], [[Brinedeep Bottom-Feeder]] and [[Fathom Dweller]]
::* 269 for [[Reins of the Azure Water Strider]] and [[Reins of the Crimson Water Strider]]
::* 284 for [[Chauffeured Chopper]] and [[Chauffeured Mechano-Hog]]
::* 398 for [[Kua'fon's Harness]]
::* 402 for [[Dragonriding]]
::* 407 for [[Deepstar Polyp]] and [[Otterworldly Ottuk Carrier]]
::* 408 for [[Unsuccessful Prototype Fleetpod]]
::* 412 for [[Otto (item)|Otto]] and [[Ottuk]]
::* 424 for [[Dragonriding]] mounts, including mounts that have dragonriding animations but are not yet enabled for dragonriding.
::* 436 for [[Wondrous Wavewhisker]]
:;uiModelSceneID:{{apitype|number}} : [[ModelSceneID]]
:;animID:{{apitype|number}}
:;spellVisualKitID:{{apitype|number}}
:;disablePlayerMountPreview:{{apitype|boolean}}

==Patch changes==
* {{Patch 8.2.5|note=Added <code>animID, spellVisualKitID, disablePlayerMountPreview</code> returns.}}
* {{Patch 7.0.3|note=Moved to <code>C_MountJournal.GetMountInfoExtraByID()</code>}}
* {{Patch 6.0.2|note=Added <code>C_MountJournal.GetMountInfoExtra()</code>}}
```