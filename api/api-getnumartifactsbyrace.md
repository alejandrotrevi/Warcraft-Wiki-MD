# API GetNumArtifactsByRace

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the amount of artifacts the player has acquired from the provided race.
 numProjects = GetNumArtifactsByRace(raceIndex)

==Arguments==
:;raceIndex:{{apitype|number}} - Index of the race to be selected.

==Returns==
:;numProjects:{{apitype|number}} - Number of artifacts for that race.

==Details==
* Opening the Archaeology window populates the values.
* The value returned is the number of completed artifacts for that race plus one for the in progress artifact. If the player hasn't collected the race's fragments yet, the value will be 0.
* Artifacts are only counted once so no matter how many times an artifact has been repeated it counts as one.
```