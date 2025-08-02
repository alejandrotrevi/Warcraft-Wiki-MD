# API GetActionBarToggles

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the enabled states for the extra action bars.
 bar1, bar2, bar3, bar4, bar5, bar6, bar7 = GetActionBarToggles()

==Returns==
:;bar1:{{apitype|boolean}} - True if the left-hand bottom action bar is shown, false otherwise.
:;bar2:{{apitype|boolean}} - True if the right-hand bottom action bar is shown, false otherwise.
:;bar3:{{apitype|boolean}} - True if the first (outer) right side action bar is shown, false otherwise.
:;bar4:{{apitype|boolean}} - True if the second (inner) right side action bar is shown, false otherwise.
:;bar5:{{apitype|boolean}}
:;bar6:{{apitype|boolean}}
:;bar7:{{apitype|boolean}}
```