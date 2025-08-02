# API BNGetInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the player's own Battle.net info.
 presenceID, battleTag, toonID, currentBroadcast, bnetAFK, bnetDND, isRIDEnabled = BNGetInfo()

==Returns==
:;presenceID:{{apitype|number?}} - Your presenceID - appears to be always nil in 8.1.5
:;battleTag:{{apitype|string}} - A nickname and number that when combined, form a unique string that identifies the friend (e.g., "Nickname#0001")
:;toonID:{{apitype|number}} - Your toonID
:;currentBroadcast:{{apitype|string}} - the current text in your broadcast box
:;bnetAFK:{{apitype|boolean}} - true if you're flagged "Away"
:;bnetDND:{{apitype|boolean}} - true if you're flagged "Busy"
:;isRIDEnabled:{{apitype|boolean}}
```