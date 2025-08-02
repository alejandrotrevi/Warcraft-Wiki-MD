# API C Spell.GetDeadlyDebuffInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Needs summary.
 deadlyDebuffInfo = C_Spell.GetDeadlyDebuffInfo(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}

==Returns==
:;deadlyDebuffInfo:{{apitype|DeadlyDebuffInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|criticalTimeRemainingMs}} || {{apitype|number?}} || 
|-
| {{apiname|criticalStacks}} || {{apitype|number?}} || 
|-
| {{apiname|priority}} || {{apitype|number}} || 
|-
| {{apiname|warningText}} || {{apitype|string}} || 
|-
| {{apiname|soundKitID}} || {{apitype|number?}} || 
|}
```