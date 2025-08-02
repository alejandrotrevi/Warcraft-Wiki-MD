# API GetSchoolString

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the name of the specified damage school mask.
 school = GetSchoolString(schoolMask)

==Arguments==
:;schoolMask:{{apitype|number}} - bitfield mask of [[Magic schools#Multi-school|damage types]].

==Returns==
:;school:{{apitype|string}} - localized school name (e.g. "Frostfire"), or "Unknown" if the school combination isn't named.

==Patch changes==
* {{Patch 5.2.0|note=Added; replaces the FrameXML global <code>SchoolStringTable</code><sup>[https://github.com/Gethe/wow-ui-source/commit/a45d7cfba2ec69944e9428b77f5d9a1b993ace0c#diff-a14fcf2d9781ea09ae9037e4c19df43f]</sup>.}}
```