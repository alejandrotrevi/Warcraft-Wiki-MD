# API TaxiNodePosition

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the position of a flight point on the taxi map.
 x, y = TaxiNodePosition(index)

==Arguments==
:;index:{{apitype|number}} - index of a flight point between 1 and {{api|NumTaxiNodes}}()

==Returns==
:;x:{{apitype|number}} - Horizontal coordinate of the taxi note (as a proportion of the taxi map's width; 0 = left edge, 1 = right edge)
:;y:{{apitype|number}} - Vertical coordinate of the taxi note (as a proportion of the taxi map's width; 0 = bottom edge, 1 = top edge)
```