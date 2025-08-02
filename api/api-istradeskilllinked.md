# API IsTradeSkillLinked

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the tradeskill being viewed is from a link along with the player's name, nil otherwise.
 isLink, playerName = IsTradeSkillLinked()

----
;''Arguments''

: none

----
;''Returns''

: isLink - 1 if the tradeskill shown in the UI is from a link (in chat), nil otherwise
: playerName - The name of the player the tradeskill link is for if isLink is 1, nil otherwise.

----
;''Example''

 if not IsTradeSkillLinked() then
     -- do something with the player's tradeskills
 end
```