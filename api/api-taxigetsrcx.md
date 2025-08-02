# API TaxiGetSrcX

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the horizontal position of the source node of a given route to the destination.
 sX = TaxiGetSrcX([destinationIndex, routeIndex])

==Arguments==
:;destinationIndex:{{apitype|number?}} - The final destination taxi node.
:;routeIndex:{{apitype|number?}} - The index of the route to get the source from.

==Returns==
:;sX:{{apitype|number}} - The horizontal position of the source node.
```