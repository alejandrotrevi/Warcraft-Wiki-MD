# API GetBattlefieldWinner

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the winner of the battlefield that the player is currently in.
 winner = GetBattlefieldWinner()

==Returns==
:;winner:{{apitype|number?}} - Faction/team that has won the battlefield. Results are: nil if nobody has won, 0 for Horde, 1 for Alliance and 255 for a draw in a battleground, 0 for Green Team and 1 for Yellow in an arena.
```