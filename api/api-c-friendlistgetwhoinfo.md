# API C FriendList.GetWhoInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_FriendList|system=FriendList}}
Retrieves info about a character on your current /who list.
 info = C_FriendList.GetWhoInfo(index)

==Arguments==
:;index:{{apitype|number}} - Index 1 up to {{api|C_FriendList.GetNumWhoResults}}()

==Returns==
:;info:{{apitype|WhoInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|fullName}} || {{apitype|string}} || Character-Realm name
|-
| {{apiname|fullGuildName}} || {{apitype|string}} || Guild name
|-
| {{apiname|level}} || {{apitype|number}} || 
|-
| {{apiname|raceStr}} || {{apitype|string}} || 
|-
| {{apiname|classStr}} || {{apitype|string}} || Localized class name
|-
| {{apiname|area}} || {{apitype|string}} || The character's current zone
|-
| {{apiname|filename}} || {{apitype|string?}} || Localization-independent  [[API_UnitClass|classFilename]]
|-
| {{apiname|gender}} || {{apitype|number}} || [[API_UnitSex|Sex]] of the character. 2 for male, 3 for female
|-
| {{apiname|timerunningSeasonID}} || {{apitype|number?}} || <font color="green">10.2.7</font>
|}

==Example==
<syntaxhighlight lang="lua">
local p = C_FriendList.GetWhoInfo(1)
print(format("%s (level %d %s %s) is in %s", p.fullName, p.level, p.raceStr, p.classStr, p.area))
</syntaxhighlight>
 > Nartan-Ravenholdt (level 43 Kul Tiran Druid) is in Eastern Plaguelands

==Patch changes==
* {{Patch 8.1.0|note=Moved to <code>C_FriendList.GetWhoInfo()</code><sup>[https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#171]</sup>}}
* {{Patch 1.0.0|note=Added as <code>GetWhoInfo()</code>}}

==See also==
* {{api|C_FriendList.SendWho}}()
* [[MACRO who|/who]]
```