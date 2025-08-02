# API C ClassColor.GetClassColor

**Contributor:** Mattsta

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassColor|system=ClassColor}}
Returns a ColorMixin for a class.
 classColor = C_ClassColor.GetClassColor(className)

==Arguments==
:;className:{{apitype|string}} : [[ClassId|classFilename]]

==Returns==
:;classColor:{{apitype|ColorMixin}} - Returns nil with invalid input.

==Example==
 /dump C_ClassColor.GetClassColor("PRIEST")
<syntaxhighlight lang="lua">
{
	r = 1,
	g = 1,
	b = 1,
	GenerateHexColor() = "ffffffff",
	-- and more ColorMixin methods
}
</syntaxhighlight>

==Patch changes==
* {{Patch 8.1.5|note=Added.}}

==See also==
* [[Class colors]] - Complete list of values
* {{api|GetClassColor}}()
```