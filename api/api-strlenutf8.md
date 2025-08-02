# API strlenutf8

**Contributor:** Kaydeethree

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} <!-- or {{wowapievent}}, {{luapi}}, {{widgethandler}}, {{widgetmethod}}, {{framexmlfunc}} -->
Returns the number of characters in a UTF8-encoded string.
 amount = strlenutf8(str)

==Arguments==
:;str:{{apitype|string}} - UTF8-encoded string.

==Returns==
:;amount:{{apitype|number}} - Number of characters in string.

==Example==
<syntaxhighlight lang="lua">
local amount = strlenutf8("Banana")
print("Count:", amount)
-- Count: 6
</syntaxhighlight>

==Details==
For many operations, '''[[API strlen|strlen]]''' may suffice. However; with non-English localization and accented player names, '''strlen''' may not return the correct amount of characters.

Non-accented Latin Characters:
<syntaxhighlight lang="lua">
print("Count:", strlen("The Lich King")) -- Count: 13
print("Count:", strlenutf8("The Lich King")) -- Count: 13
</syntaxhighlight>


Accented Latin Characters:
<syntaxhighlight lang="lua">
print("Count:", strlen("Der Lichkönig")) -- Count: 14 (incorrect)
print("Count:", strlenutf8("Der Lichkönig")) -- Count: 13
</syntaxhighlight>

==See Also==
[[Lua functions#String_Functions]]

==External Links==
{{elink|type=wowus|link=https://us.battle.net/support/en/article/34530|desc=World of Warcraft Naming Policy}}
{{elink|site=Unicode.org|link=https://www.unicode.org/charts/nameslist/|desc=Unicode Names List Charts}}
```