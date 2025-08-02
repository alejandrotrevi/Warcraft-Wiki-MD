# API GetWhoInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
#REDIRECT [[API_C_FriendList.GetWhoInfo]]
{{wowapi}}
Retrieve info about a character on your current /who list.
 name, guild, level, race, class, zone, classFileName, sex = GetWhoInfo(index)

== Arguments ==
;index : Number - /who result index, ascending from 1.

== Returns ==
; name : String - Name of the character.
; guild : String - Guild name of the character.
; level : Number - Level of the character
; race : String - Race of the character.
; class : String - Class of the character.
; zone : String - Zone the character was in at query time.
; classFileName : String - Uppercase english classname of the character.
; sex : Number - Sex of the character. 2 for male, 3 for female.

== See also ==
* {{api|SendWho}}
* {{api|SortWho}}
```