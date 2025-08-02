# API GetFriendshipReputation

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a friendship reputation.
 friendID, friendRep, friendMaxRep, friendName, friendText, friendTexture, friendTextLevel, friendThreshold, nextFriendThreshold = GetFriendshipReputation(factionID)

==Arguments==
:;factionID:{{apitype|number}} : [[FactionID]] - A subset of these IDs are friendship reputations.

==Returns==
:;friendID:{{apitype|number}} - ID of the friendship
:;friendRep:{{apitype|number}} - Total reputation the player has earned with the friend
:;friendMaxRep:{{apitype|number}} - Maximum reputation that can be earned with the friend
:;friendName:{{apitype|string}} - Name of the friend
:;friendText:{{apitype|string}} - Description of the friend, as shown in the tooltip that appears when you mouse over the friend row
:;friendTexture:{{apitype|number}} - The [[fileID]] of the icon texture for this faction
:;friendTextLevel:{{apitype|string}} - Text of the player's current standing with the friend
:;friendThreshold:{{apitype|number}} - Minimum reputation required to reach the current standing
:;nextFriendThreshold:{{apitype|number}} - Maximum reputation that can be earned with the friend before graduating to the next standing, nil if at max rank

==See also==
* {{api|GetFactionInfo}}
* {{api|GetFriendshipReputationRanks}}

==Patch changes==
* {{Patch 7.3.0|note=The icon texture is no longer a string, but a [[fileID]] instead.}}
* {{Patch 5.1.0|note=Added}}
```