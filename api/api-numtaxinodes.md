# API NumTaxiNodes

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of flight paths on the taxi map.
 numNodes = NumTaxiNodes()

==Returns==
:;numNodes:{{apitype|number}} - total number of flight points on the currently open taxi map; 0 if the taxi map is not open.

==Details==
* Taxi information is only available while the taxi map is open -- between the {{api|t=e|TAXIMAP_OPENED}} and {{api|t=e|TAXIMAP_CLOSED}} events.

==See also==
* {{api|TaxiNodeName}}
* {{api|TaxiNodePosition}}
* {{api|TakeTaxiNode}}
```