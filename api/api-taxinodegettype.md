# API TaxiNodeGetType

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the type of a flight path node.
 type = TaxiNodeGetType(index)

==Arguments==
:;index:{{apitype|number}} - Taxi map node index, ascending from 1 to {{api|NumTaxiNodes}}().

==Returns==
:;type:{{apitype|string}} - "CURRENT" for the player's current position, "REACHABLE" for nodes that can be travelled to, "DISTANT" for nodes that can't be travelled to, and "NONE" if the index is out of bounds.

==Details==
* Taxi information is only available while the taxi map is open -- between the {{api|t=e|TAXIMAP_OPENED}} and {{api|t=e|TAXIMAP_CLOSED}} events.

==See also==
* {{api|TaxiNodeName}}
```