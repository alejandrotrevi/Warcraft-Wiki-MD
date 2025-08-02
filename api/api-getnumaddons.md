# API GetNumAddOns

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Get the number of user supplied AddOns.
 count = GetNumAddOns()

==Returns==
:;count:{{apitype|number}} - The number of user supplied AddOns installed. This is the maximum valid index to the other AddOn functions. This count does NOT include Blizzard supplied UI component AddOns.

{{apinavbox|AddOn}}
```