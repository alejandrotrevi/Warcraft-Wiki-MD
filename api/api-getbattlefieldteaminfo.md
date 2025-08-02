# API GetBattlefieldTeamInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an Arena team at the end of the match.
 teamName, oldTeamRating, newTeamRating, teamRating = GetBattlefieldTeamInfo(index)

==Arguments==
:;index:{{apitype|number}} - Which team to get information on, 0 is Green team and 1 is Gold Team

==Returns==
:;teamName:{{apitype|string}} - Teams name inside a rated arena match.
:;oldTeamRating:{{apitype|number}} - Old rating that the team entered with (0 is no team is found)
:;newTeamRating:{{apitype|number}} - New rating that the team is leaving with
:;teamRating:{{apitype|number}} - Formerly known as ''match making rating''

==Details==
This cannot be used until the arena has ended and UPDATE_BATTLEFIELD_SCORE is fired, if for some reason a game ends as soon as it starts with no enemy team joining, oldTeamRating will be 0.
```