# API SetTalentGroupRole

**Contributor:** DokoNinjaroboto

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the role for a player talent group (primary or secondary).
 SetTalentGroupRole(groupIndex, role)

==Arguments==
:;groupIndex:{{apitype|number}} - Ranging from <code>1</code> to <code>2</code> (primary/secondary talent group). To get the current one use {{api|GetActiveTalentGroup}}()
:;role:{{apitype|string}} - Can be <code>DAMAGER</code>, <code>TANK</code>, or <code>HEALER</code>. If an invalid role is given, it defaults to <code>DAMAGER</code>
```