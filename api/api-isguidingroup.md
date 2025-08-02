# API IsGUIDInGroup

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether or not the unit with the given GUID is in your group.
 inGroup = IsGUIDInGroup(guid [, groupType])

==Arguments==
:;guid:{{apitype|WOWGUID}}
:;groupType:{{apitype|number?}}
{{:LE_PARTY_CATEGORY|nocaption=1}}

==Returns==
:;inGroup:{{apitype|boolean}} - True if the given GUID is in your group, considering groupType if provided, otherwise false.

==Details==
{| {{apitable}} border: 0px;"
{{apirow | Related API | {{api|UnitGUID}} }}
{{apirow | Related Event | {{api|t=e|GROUP_ROSTER_UPDATE}} }}
|}
```