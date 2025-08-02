# API GetNumGlyphSockets

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of glyph sockets the player will have access to at max level.
 numGlyphSockets = GetNumGlyphSockets()

== Returns ==
:;numGlyphSockets:{{apitype|number}} - Number of glyph sockets the player will have access to at max level.

==Details==
* Sockets have individual level requirements; not every socket may be usable at the character's particular level.
* Returns the same value as <code>NUM_GLYPH_SLOTS</code>.
```