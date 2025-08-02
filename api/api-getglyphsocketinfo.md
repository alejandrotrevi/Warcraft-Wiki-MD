# API GetGlyphSocketInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information on a glyph socket.
 enabled, glyphType, glyphIndex, glyphSpellID, iconFile, glyphID = GetGlyphSocketInfo(socketID [, talentGroup])

==Arguments==
:;socketID:{{apitype|number}} - The socket index to query, ranging from 1 through <code>NUM_GLYPH_SLOTS</code>.
:;talentGroup:{{apitype|number?}} - The talent specialization group to query. Defaults to 1.

==Returns==
:;enabled:{{apitype|boolean}} - True if the socket has a glyph inserted.
:;glyphType:{{apitype|number}} - The type of glyph accepted by this socket. Either <code>1</code> Major, <code>2</code> Minor, or <code>3</code> Prime,
:;glyphIndex:{{apitype|number}} - The sockets index for the glyph type's. Either <code>0</code>, <code>1</code>, <code>2</code>.
:;glyphSpellID:{{apitype|number?}} - The spell ID of the socketed glyph.
:;iconFile:{{apitype|fileID?}} - The file ID of the sigil icon associated with the socketed glyph.
:;glyphID:{{apitype|number}}

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 7.0.3|note=Removed.}}
* {{Patch 5.0.3|note=Added <code>isInspect</code> and <code>inspectUnit</code> arguments.}}
* {{Patch 4.0.6|note=Added <code>glyphID</code> return value.}}
* {{Patch 4.0.3|note=Added <code>glyphTooltipIndex</code> return value before <code>glyphSpellID</code>.}}
* {{Patch 3.1.0|note=Added <code>talentGroup</code> argument.}}
* {{Patch 3.0.2|note=Added.}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 5.5.0|note=Added <code>glyphID</code> in beta build 5.5.0 (61135).}}
* {{Patch 3.4.0|note=Added.}}
```