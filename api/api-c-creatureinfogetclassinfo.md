# API C CreatureInfo.GetClassInfo

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CreatureInfo|system=CreatureInfo}}
Returns info for a class by ID.
 classInfo = C_CreatureInfo.GetClassInfo(classID)

==Arguments==
:;classID:{{apitype|number}} : [[ClassId]] - Ranging from 1 to the highest classID. For Retail, that's the same as {{api|GetNumClasses}}().

==Returns==
:;classInfo:{{apitype|ClassInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| className || {{apitype|string}} || Localized name, e.g. <code>"Warrior"</code> or <code>"Guerrier"</code>.
|-
| classFile || {{apitype|string}} || Locale-independent name, e.g. <code>"WARRIOR"</code>.
|-
| classID || {{apitype|number}} || 
|}

==Values==
{{:ClassId}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

{{apinavbox|Class}}
```