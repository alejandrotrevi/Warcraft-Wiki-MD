# API UnitSex

**Contributor:** Kaydeethree

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the gender of the unit.
 gender = UnitSex(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;sex:{{apitype|number?}}
<onlyinclude>{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! ID !! Gender
|-
| 1 || Neutrum / Unknown
|-
| 2 || Male
|-
| 3 || Female
|}</onlyinclude>

==Example==
<syntaxhighlight lang="lua">
/run local genders = {"unknown", "male", "female"} if UnitExists("target") then print(UnitName("target"), "is", genders[UnitSex("target")]) end
</syntaxhighlight>

==Details==
* Most non-humanoid mobs/creatures will appear as Neutrum/Unknown.
* Player characters currently appear as either Male or Female.

==Patch changes==
* {{Patch 1.11|note=Return values changed to 1 unknown, 2 male, 3 female|comment=Previously returned 0 male, 1 female, 2 unknown}}
* At an unknown time after 1.10, sheeped targets stopped returning 'unknown' and began providing the 'true' gender

==See also==
* {{api|C_PlayerInfo.GetSex}}()
```