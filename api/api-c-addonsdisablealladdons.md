# API C AddOns.DisableAllAddOns

**Contributor:** Ghostopheles

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=AddOns}}
Sets all addons to be disabled.
 C_AddOns.DisableAllAddOns([character])

==Arguments==
:;character:{{apitype|string?}} - The name or [[GUID]] of the character, excluding the realm name. If omitted, disables all addons for all characters.

==Details==
: All addons will be disabled on the next session, when reloading or relogging.
```