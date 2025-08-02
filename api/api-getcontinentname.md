# API GetContinentName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of the continent from the provided continent ID.
 continent = GetContinentName(continentID)

==Arguments==
:;continentID:{{apitype|number}} - A continent's unique ID.

==Returns==
:;continent:{{apitype|string}} - The name of the continent.

==Example==
 local continents = { GetMapContinents() }
 for i=1,#continents / 2 do
  print("#"..i.." "..GetContinentName(i))
 end

==Results==
 #1 Kalimdor
 #2 Eastern Kingdoms
 #3 Outland
 #4 Northrend
 #5 The Maelstrom
 #6 Pandaria
 #7 Draenor
 #8 Broken Isles
 #9 Argus

==Details==
* Note that as more expansions are released, the output of this function will probably change. Also, the output differs based on the [[localization]] of the client.
* The order continents are returned in corresponds to the {{api|GetCurrentMapContinent}} return values.
```