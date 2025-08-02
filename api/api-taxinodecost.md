# API TaxiNodeCost

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the cost of the flight path in copper.
   cost = TaxiNodeCost(slot)

==Arguments==
:;slot:{{apitype|number}} - 1 ascending to {{api|NumTaxiNodes}}(), out of bound numbers triggers lua error.

==Returns==
:;cost:{{apitype|number}} - returns the cost in copper, 0 if destination is undiscovered, free or current node.

==Example==
The following example will print the name and cost for each flight point that is not free.
  for i= 1, NumTaxiNodes() do
    if (TaxiNodeCost(i) > 0) then
      print(format("Flight to %s costs: %s", TaxiNodeName(i), GetCoinText(TaxiNodeCost(i)," ")))
    end
  end
==Details==
* Taxi information is only available while the taxi map is open -- between the [[TAXIMAP_OPENED]] and [[TAXIMAP_CLOSED]] events.
* "invalid taxi node slot" is an error triggered by out-of-bound slot (0 or NumTaxiNodes() < slot) or if there is no taxi map open.
* For some reason, this returns the original cost of the given slot, not taking into account any reductions you get due to faction. -pircio

==See also==
*{{api|NumTaxiNodes}}()
*{{api|TaxiNodeGetType}}(slot)
*{{api|TaxiNodeName}}(slot)
```