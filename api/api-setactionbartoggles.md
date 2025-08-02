# API SetActionBarToggles

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the visible state for each action bar.
 SetActionBarToggles([bar1, bar2, bar3, bar4, bar5, bar6, bar7, alwaysShow])

==Arguments==
:;bar1:{{apitype|boolean}} - true if the left-hand bottom action bar is to be shown, false otherwise.
:;bar2:{{apitype|boolean}} - true if the right-hand bottom action bar is to be shown, false otherwise.
:;bar3:{{apitype|boolean}} - true if the first (outer) right side action bar is to be shown, false otherwise.
:;bar4:{{apitype|boolean}} - true if the second (inner) right side action bar is to be shown, false otherwise.
:;bar5:{{apitype|boolean}}
:;bar6:{{apitype|boolean}}
:;bar7:{{apitype|boolean}}
:;alwaysShow:{{apitype|string}} - true if the bars are always shown, false otherwise.

==Details==
: Note that this doesn't actually change the action bar states directly, it simply registers the desired states for the next time the game is loaded. The states during play are in the variables <code>SHOW_MULTI_ACTIONBAR_1, SHOW_MULTI_ACTIONBAR_2, SHOW_MULTI_ACTIONBAR_3, SHOW_MULTI_ACTIONBAR_4</code>, and reflected by calling MultiActionBar_Update().
```