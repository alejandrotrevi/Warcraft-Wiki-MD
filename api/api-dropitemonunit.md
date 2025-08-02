# API DropItemOnUnit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Drops an item from the cursor onto a unit, i.e. to initiate a trade.
 DropItemOnUnit(unit)

==Parameters==
===Arguments===
:;unit:{{apitype|string}} : [[UnitId]] - Unit to which you want to give the item on the cursor. 
==Example==
 if ( CursorHasItem() ) then
   DropItemOnUnit("pet");
 end;
===Result===
Item is dropped from cursor and given to the player's pet.
```