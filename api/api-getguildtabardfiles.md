# API GetGuildTabardFiles

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns File IDs of tabard textures used in guild bank logo.
 tabardBackgroundUpper, tabardBackgroundLower, tabardEmblemUpper, tabardEmblemLower, tabardBorderUpper, tabardBorderLower = GetGuildTabardFiles()

==Returns==
:;tabardBackgroundUpper:{{apitype|number}} : [[FileID]]
:;tabardBackgroundLower:{{apitype|number}} : FileID
:;tabardEmblemUpper:{{apitype|number}} : FileID
:;tabardEmblemLower:{{apitype|number}} : FileID
:;tabardBorderUpper:{{apitype|number}} : FileID
:;tabardBorderLower:{{apitype|number}} : FileID

==Patch changes==
* {{Patch 8.2.0|note=Replaced texture paths with FileDataIDs.}}
```