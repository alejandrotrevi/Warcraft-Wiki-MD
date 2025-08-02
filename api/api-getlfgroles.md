# API GetLFGRoles

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the roles the player signed up for in the Dungeon Finder.
 isLeader, isTank, isHealer, isDPS = GetLFGRoles()

==Returns==
:;isLeader:{{apitype|boolean}}  - if you signed up as a candidate for group leader
:;isTank:{{apitype|boolean}} - if you signed up as a tank
:;isHealer:{{apitype|boolean}} - if you signed up as a healer
:;isDPS:{{apitype|boolean}} - if you signed up as DPS
```