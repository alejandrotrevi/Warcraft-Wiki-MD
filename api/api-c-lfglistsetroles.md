# API C LFGList.SetRoles

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGList|system=LFGList}}
Sets the player's Group Finder roles
 success = C_LFGList.SetRoles(roles)

==Arguments==
:;roles:{{apitype|LFGRoles}} - A table with each role as a {{apitype|string}} key, and a {{apitype|boolean}} value for whether that role should be selected. All roles must be present in the table.
{{:Struct LFGRoles|nocaption=1}}

==Returns==
:;success:{{apitype|boolean}} - Whether setting the roles was successful or not
```