# API TaxiGetSrcY

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the vertical position of the source node of a given route to the destination.
 sY = TaxiGetSrcY([destinationIndex, routeIndex])

==Arguments==
:;destinationIndex:{{apitype|number?}} - The final destination taxi node.
:;routeIndex:{{apitype|number?}} - The index of the route to get the source from.

==Returns==
:;sY:{{apitype|number}} - The vertical position of the source node.
```