# API GetFriendshipReputationRanks

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the (max) rank for a friendship reputation.
 currentRank, maxRank = GetFriendshipReputationRanks([factionID])

[[Image:API_GetFriendshipReputationRanks.png|frame|right|[https://www.townlong-yak.com/framexml/go/ShowFriendshipReputationTooltip ShowFriendshipReputationTooltip]]]

==Arguments==
:;factionID:{{apitype|number?}} : [[FactionID]] - A subset of these IDs are friendship reputations. Defaults to the currently interacting NPC if omitted

==Returns==
:;currentRank:{{apitype|number}}
:;maxRank:{{apitype|number}} - Can go up to 10, depending on the friendship faction.

==Details==
* Rank names for the [[Tillers]] friendships.
{| class="sortable darktable zebra col1-center"
! Index !! Name
|-
| 1 || Stranger
|-
| 2 || Acquaintance
|-
| 3 || Buddy
|-
| 4 || Friend
|-
| 5 || Good Friend
|-
| 6 || Best Friend
|}

==Example==
* Prints an example output.
<syntaxhighlight lang="lua">
/dump GetFriendshipReputationRanks(1273) -- 1, 6 (Jogu the Drunk)
/dump GetFriendshipReputationRanks(1374) -- 1, 10 (Brawl'gar Arena)
</syntaxhighlight>

* Prints the friendship reputations for your character.
<syntaxhighlight lang="lua">
for i = 1, GetNumFactions() do
	local factionID = select(14, GetFactionInfo(i))
	local friendID, _, _, name = GetFriendshipReputation(factionID)
	if friendID then
		local currentRank, maxRank = GetFriendshipReputationRanks(friendID)
		print(friendID, name, currentRank, maxRank)
	end
end
</syntaxhighlight>

==See also==
* {{api|GetFactionInfo}}
* {{api|t=a|GetFriendshipReputation}}

==Patch changes==
* {{Patch 5.1.0|note=Added (PTR [https://github.com/tekkub/wow-ui-source/commit/248d2d6e32fa516b4a36b3d8fcf5324a126872ff#L48R505 5.1.0.16139])}}
```