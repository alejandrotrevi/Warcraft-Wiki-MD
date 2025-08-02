# API C AuctionHouse.SearchForFavorites

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|noscript|note=Otherwise it will brick the AH.}}
Searches for favorited items.
 C_AuctionHouse.SearchForFavorites(sorts)

==Arguments==
:;sorts:{{apitype|AuctionHouseSortType[]}}
{{:Struct AuctionHouseSortType|nocaption=1}}

==Example==
Searches for favorites.
<syntaxhighlight lang="lua">
function Example() -- /run Example()
	C_AuctionHouse.SearchForFavorites({})
end
</syntaxhighlight>

Sorts by price (ascending), and then name (descending).
<syntaxhighlight lang="lua">
local sorts = {
	{sortOrder = Enum.AuctionHouseSortOrder.Price, reverseSort = false},
	{sortOrder = Enum.AuctionHouseSortOrder.Name, reverseSort = true},
}

function Example() -- /run Example()
	C_AuctionHouse.SearchForFavorites(sorts)
end
</syntaxhighlight>

[[File:API C_AuctionHouse.SearchForFavorites.png]]

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```