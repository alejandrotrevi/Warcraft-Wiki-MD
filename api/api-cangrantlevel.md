# API CanGrantLevel

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether you can grant levels to a particular player.
 status = CanGrantLevel(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;status:{{apitype|boolean}} - true if you can grant levels to the unit; nil otherwise (unit is not RAF-linked to you, does not meet level requirements, or you are out of levels to grant).

==Example==
The snippet below prints whether you can grant levels to your target right now.
 local status = CanGrantLevel("target")
 if status then
  print("I can grant levels to my friend!")
 else
  print("I am out of free levels for now.")
 end
```