# API GetBattlefieldFlagPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Used to position the flag icon on the world map and the battlefield minimap.
 flagX, flagY, flagToken = GetBattlefieldFlagPosition(index)

===Arguments===
:;index:{{apitype|number}} - Index to get the flag position from

===Returns===
:;flagX:{{apitype|number}} - Position of the flag on the map.
:;flagY:{{apitype|number}} - Position of the flag on the map.
:;flagToken:{{apitype|string}} - Name of flag texture in Interface\WorldStateFrame\

:: In Warsong Gulch the names of the flag textures are the strings "AllianceFlag" and "HordeFlag".
```