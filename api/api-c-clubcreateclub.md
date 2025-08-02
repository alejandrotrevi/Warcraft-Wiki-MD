# API C Club.CreateClub

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Club|system=Club}} {{restrictedapi|protected}}
Needs summary.
 C_Club.CreateClub(name, shortName?, description, clubType, avatarId [, isCrossFaction])

==Arguments==
:;name:{{apitype|string}}
:;shortName:{{apitype|string?}}
:;description:{{apitype|string}}
:;clubType:{{apitype|Enum.ClubType}} - Valid types are BattleNet or Character
{{:Enum.ClubType|nocaption=1}}
:;avatarId:{{apitype|number}}
:;isCrossFaction:{{apitype|boolean?}}

==Patch changes==
* {{Patch 9.2.5|note=Added <code>isCrossFaction</code> argument.}}
* {{Patch 8.0.1|note=Added.}}
```