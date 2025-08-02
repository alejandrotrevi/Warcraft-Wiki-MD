# API TaxiGetDestY

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the vertical position of the destination node of a given route to the destination.
 dY = TaxiGetDestY(destinationIndex, routeIndex)

==Arguments==
:;destinationIndex:{{apitype|number?}} - The final destination taxi node.
:;routeIndex:{{apitype|number?}} - The index of the route to get the source from.

==Returns==
:;dY:{{apitype|number}} - The vertical position of the destination node for the route.
```