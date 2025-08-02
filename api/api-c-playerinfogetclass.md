# API C PlayerInfo.GetClass

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the class of a player.
 className, classFilename, classID = C_PlayerInfo.GetClass(playerLocation)

==Arguments==
:;playerLocation:{{apitype|PlayerLocationMixin}}

==Returns==
:;className:{{apitype|string?}}
:;classFilename:{{apitype|string?}}
:;classID:{{apitype|number?}} : [[ClassId]]

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```