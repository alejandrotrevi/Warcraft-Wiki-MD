# API GetPVPYesterdayStats

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the character's Honor statistics for yesterday.
 honorableKills, dishonorableKills = GetPVPYesterdayStats()

==Returns==
:;honorableKills:{{apitype|number}} - The number of honorable kills
:;dishonorableKills:{{apitype|number}} - The number of dishonorable kills

==Patch changes==
* Removed <code>contribution</code> (third return value) in an unknown patch.
```