# API GetSocketTypes

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the type (color) of a socket in the item.
 gemColor = GetSocketTypes(index)

==Arguments==
:;index:{{apitype|number}} - Index between 1 and {{api|GetNumSockets}}

==Returns==
:;gemColor:{{apitype|string}} - The type of the socket at position Index.  The value could be any of these (apparently unlocalized) strings: 
:::"Red" - Red socket
:::"Yellow" - Yellow socket
:::"Blue" - Blue socket
:::"Meta" - Meta socket
:::"Socket" - Prismatic socket

==Details==
: This function is only useful if the item socketing window is currently visible.
```