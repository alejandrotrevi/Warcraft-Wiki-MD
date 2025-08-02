# API GetHomePartyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns names of characters in your home (non-instance) party.
 homePlayers = GetHomePartyInfo([homePlayers])

==Arguments==
:;homePlayers:{{apitype|table}} - table to populate and return; a new table is created if this argument is omitted.

==Returns==
:;homePlayers:{{apitype|table}} - array containing your (non-instance) party members' names, or nil if you're not in any non-instance party.

==Patch changes==
* {{Patch 5.1.0|note=Added.}}
```