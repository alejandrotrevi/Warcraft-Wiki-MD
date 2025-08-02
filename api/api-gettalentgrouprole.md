# API GetTalentGroupRole

**Contributor:** DokoNinjaroboto

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the currently select role for a player talent group (primary or secondary).
 role = GetTalentGroupRole(groupIndex)

==Arguments==
:;groupIndex:{{apitype|number}} - Ranging from <code>1</code> to <code>2</code> (primary/secondary talent group). To get the current one use {{api|GetActiveTalentGroup}}()

==Returns==
:;role:{{apitype|string}} - Can be <code>DAMAGER</code>, <code>TANK</code>, or <code>HEALER</code>
```