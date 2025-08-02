# API GetPetitionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the petition being viewed.
 petitionType, title, bodyText, maxSigs, originator, isOriginator, minSigs = GetPetitionInfo()

==Returns==
:;petitionType:{{apitype|string}} - The type of petition (ex. "guild" or "arena")
:;title:{{apitype|string}} - The title of the group being created
:;bodyText:{{apitype|string}} - The body text of the petition
:;maxSigs:{{apitype|number}} - The maximum number of signatures allowed on the petition
:;originator:{{apitype|string}} - The name of the person who started the petition
:;isOriginator:{{apitype|boolean}} - Whether the player is the originator of the petition
:;minSigs:{{apitype|number}} - The minimum number of signatures required for the petition

==See also==
* {{api|t=e|PETITION_SHOW}} - Indicates information is available.
```