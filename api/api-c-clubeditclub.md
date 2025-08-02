# API C Club.EditClub

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 C_Club.EditClub(clubId [, name [, shortName [, description [, avatarId [, broadcast [, crossFaction]]]]]])

==Arguments==
:;clubId:{{apitype|string}}
:;name:{{apitype|string?}}
:;shortName:{{apitype|string?}}
:;description:{{apitype|string?}}
:;avatarId:{{apitype|number?}}
:;broadcast:{{apitype|string?}}
:;crossFaction:{{apitype|boolean?}}

==Details==
* nil arguments will not change existing club data

==Patch changes==
* {{Patch 9.2.5|note=Added <code>crossFaction</code> argument.}}
* {{Patch 8.0.1|note=Added.}}
```