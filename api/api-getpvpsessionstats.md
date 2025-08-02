# API GetPVPSessionStats

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the character's Honor statistics for this session.
 honorableKills, dishonorableKills = GetPVPSessionStats()

==Returns==
:;honorableKills:{{apitype|number}} - Amount of honorable kills you have today, returns 0 if you havn't killed anybody today.
:;dishonorableKills:{{apitype|number}} - ''Note: Not sure if this is '''dishonorable kills''' or '''estimated honor points for today'''''

==Details==
Used for retrieving how many honorable kills and honor points you have for today, currently the honor points value is calculated using the ''estimated'' honor points from killing an enemy player, and does not take diminishing returns or bonus honor into effect.

==Example==
Displays how many honorable kills and estimated honor points you have for today.

 local hk, hp = GetPVPSessionStats();
 DEFAULT_CHAT_FRAME:AddMessage( "You currently have " .. hk .. " honorable kills today, and an estimated " .. hp .. " honor points." );
```