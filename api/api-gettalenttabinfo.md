# API GetTalentTabInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information for a talent tab (tree).
 id, name, description, icon, pointsSpent, background, previewPointsSpent, isUnlocked = GetTalentTabInfo(index[, isInspect, isPet, talentGroup])

==Arguments==
:;index:{{apitype|number}} - Ranging from 1 to {{api|GetNumTalentTabs}}()
:;isInspect:{{apitype|boolean?}} - Optional, will return talent tab info for the current inspect target if true (see {{api|NotifyInspect}}).
:;isPet:{{apitype|boolean?}} - Optional, will return talent tab info for the players' pet if true.
:;talentGroup:{{apitype|number?}} - Optional talent group to query for [[Dual Talent Specialization]]. Defaults to <code>1</code> for the primary specialization.

==Returns==
:;id:{{apitype|number}}
:;name:{{apitype|string}}
:;description:{{apitype|string}}
:;icon:{{apitype|number}}
:;pointsSpent:{{apitype|number}} - Number of points put into the tab.
:;background:{{apitype|number}} - File name of the background image.
:;previewPointsSpent:{{apitype|number}}
:;isUnlocked:{{apitype|boolean}}

==Example==
An example of how to use the fileName return value would be<sup>[https://github.com/Gethe/wow-ui-source/blob/163ac1f68d1026f4faad2eb27a54838f080bc21a/AddOns/Blizzard_TalentUI/Blizzard_TalentUI.lua#L161-L172]</sup>
 string.format("Interface\\TalentFrame\\%s-TopLeft", fileName)

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 5.0.4|note=Removed.}}
* {{Patch 3.1.0|note=Added <code>talentGroup</code> parameter.}}
* {{Patch 3.0.2|note=Added <code>isPet</code> parameter.}}
* {{Patch 2.3.0|note=Added <code>isInspect</code> parameter.}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 4.4.0|note=Added <code>name</code>, <code>description</code>, <code>previewPointsSpent</code> and <code>isUnlocked</code> arguments.}}
* {{Patch 3.4.0|note=Added <code>isPet</code> and <code>talentGroup</code> arguments.}}
* {{Patch 2.5.1|note=Added <code>isInspect</code> argument.}}
* {{Patch 1.13.2|note=Added.}}
```