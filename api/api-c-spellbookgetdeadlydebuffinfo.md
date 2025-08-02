# API C SpellBook.GetDeadlyDebuffInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Needs summary.
 deadlyDebuffInfo = C_SpellBook.GetDeadlyDebuffInfo(spellID)

==Arguments==
:;spellID:{{apitype|number}}

==Returns==
:;deadlyDebuffInfo:{{apitype|DeadlyDebuffInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| overrideCriticalTimeRemaining || {{apitype|number}} || 
|-
| priority || {{apitype|number}} || 
|-
| warningText || {{apitype|string}} || 
|-
| soundKitID || {{apitype|number?}} || 
|}
```