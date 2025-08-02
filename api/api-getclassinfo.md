# API GetClassInfo

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a class.
 className, classFile, classID = GetClassInfo(classID)

==Arguments==
:;classID:{{apitype|number}} : [[ClassId]] - Ranging from 1 to the highest classID. For Retail, that's the same as {{api|GetNumClasses}}().

==Returns==
:;className:{{apitype|string}} - Localized name, e.g. <code>"Warrior"</code> or <code>"Guerrier"</code>.
:;classFile:{{apitype|string}} - Locale-independent name, e.g. <code>"WARRIOR"</code>.
:;classID:{{apitype|number}} : [[ClassId]]

==Details==
* {{Wow-inline}} For classes that don't exist in Classic, this function may return information for a ''different'' class, or it may return <code>nil</code>. This behaviour has changed over time, so it may be unwise to rely on the current behaviour staying the same.

==Values==
{{:ClassId}}

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

{{apinavbox|Class}}
```