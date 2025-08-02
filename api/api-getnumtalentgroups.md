# API GetNumTalentGroups

**Contributor:** DokoNinjaroboto

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the total number of talent groups for the player.
 num = GetNumTalentGroups([isInspect])

==Arguments==
:;isInspect:{{apitype|boolean?|default=false}}

==Returns==
:;num:{{apitype|number}} - The number of talent groups. <code>1</code> by default, <code>2</code> if [[Dual Talent Specialization]] is purchased.

==Details==
* Using <code>isInspect</code> requires calling {{api|NotifyInspect}}() and awaiting {{api|t=e|INSPECT_READY}}. If not done, it returns information for the player instead.
{| {{apitable}}
{{apirow | Related API | {{api|GetNumTalentTabs}} }}
|}
```