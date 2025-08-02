# API GetLFGBootProposal

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a LFG votekick in progress.
 inProgress, didVote, myVote, targetName, totalVotes, bootVotes, timeLeft, reason = GetLFGBootProposal()

==Returns==
:;inProgress:{{apitype|boolean}} - true if a Kick vote is currently in progress, false otherwise.
:;didVote:{{apitype|boolean}} - true if you have already voted, false otherwise.
:;myVote:{{apitype|boolean}} - true if you've voted to kick the player, false otherwise.
:;targetName:{{apitype|string}} - name of the player being voted on.
:;totalVotes:{{apitype|number}} - total votes cast so far.
:;bootVotes:{{apitype|number}} - votes in favor of kicking the player cast so far.
:;timeLeft:{{apitype|number}} - amount of time left to vote.
:;reason:{{apitype|string}} - reason given for initiating a vote kick vote against a player.

==Related events==
* {{api|LFG_BOOT_PROPOSAL_UPDATE|t=e}}
```