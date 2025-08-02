# API C Calendar.EventSetTextureID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 C_Calendar.EventSetTextureID(textureIndex)

==Arguments==
:;textureIndex:{{apitype|number}} - '''NOT''' a FileDataID, but an index relating to the returned table of [[API_C_Calendar.EventGetTextures]]. You cannot set a custom texture, or even one outside the [[API_C_Calendar.EventSetType|chosen event type]]. Therefore, this function currently only has an effect when using the types Raid and Dungeon.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```