# API strsplit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Splits a string using a delimiter.
 s1, s2, ... =      strsplit(delimiter, str [, pieces])
 s1, s2, ... =  string.split(delimiter, str [, pieces])
 chunks      = strsplittable(delimiter, str [, pieces])

==Arguments==
:;delimiter:{{apitype|string}} - Characters (bytes) that will be interpreted as delimiter characters (bytes) in the string.
:;str:{{apitype|string}} - String to split.
:;pieces:{{apitype|number?}} - Maximum number of pieces to make (the "last" piece would contain the rest of the string); by default, an unbounded number of pieces is returned.

==Returns==
===<font color="#4ec9b0">strsplit | string.split</font>===
:;s1, s2, ...:{{apitype|string}} - Returns a variable amount of string variables.

===<font color="#4ec9b0">strsplittable</font>===
:;chunks:{{apitype|string[]}} - Returns an array of strings.

==Example==
<syntaxhighlight lang="lua">
/dump strsplit(":", "hello:world:banana:apple", 3)
> "hello", "world", "banana:apple"
</syntaxhighlight>
<syntaxhighlight lang="lua">
/dump strsplittable(":", "hello:world:banana")
> {
	[1] = "hello",
	[2] = "world",
	[3] = "banana"
}
</syntaxhighlight>

==Details==
Note that strsplit uses a raw string as delimited, not a pattern, so it's not particularily well-suited for e.g. commandline arguments, where it should be ok to use multiple spaces. To extract whitespace-separated arguments, you can use e.g.
 local tbl = {}
 for v in string.gmatch(" this   has     lots of   space   ", "[^ ]+") do
   tinsert(tbl, v)
 end

Additionally note that the delimiter defines all bytes that will split the string, e.g.:
 strsplit("ab", "1a2b3")  -- => "1", "2", "3"
or
 strsplit("ab", "1ab2")  -- => "1", "", "2"

N.B. This function does not handle embedded NUL characters ("\0") gracefully.  If you need a unique "signpost" character embedded in your strings to be split apart later, try the ASCII bell character ("\a").  This won't show up in the game, and strsplit handles it just fine.
```