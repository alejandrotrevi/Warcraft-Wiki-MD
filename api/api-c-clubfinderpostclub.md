# API C ClubFinder.PostClub

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClubFinder|system=ClubFinderInfo}}
Needs summary.
 succesful = C_ClubFinder.PostClub(clubId, itemLevelRequirement, name, description, avatarId, specs, type [, crossFaction])

==Arguments==
:;clubId:{{apitype|string}}
:;itemLevelRequirement:{{apitype|number}}
:;name:{{apitype|string}}
:;description:{{apitype|string}}
:;avatarId:{{apitype|number}}
:;specs:{{apitype|number[]}}
:;type:{{apitype|Enum.ClubFinderRequestType}}
{{:Enum.ClubFinderRequestType|nocaption=1}}
:;crossFaction:{{apitype|boolean?|default=false}}

==Returns==
:;succesful:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.2.5|note=Added <code>crossFaction</code> return.}}
* {{Patch 9.1.0|note=Added <code>avatarId</code> argument.}}
* {{Patch 8.2.5|note=Added <code>succesful</code> return.}}
* {{Patch 8.2.0|note=Added.}}
```