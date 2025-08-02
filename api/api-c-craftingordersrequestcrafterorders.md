# API C CraftingOrders.RequestCrafterOrders

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CraftingOrders|system=CraftingOrderUI}} {{restrictedapi|noscript|note=Requests issued from dynamic scripts will result in no data being returned from subsequent calls to {{api|C_CraftingOrders.GetCrafterOrders}}.}}
Needs summary.
 C_CraftingOrders.RequestCrafterOrders(request)

==Arguments==
:;request:{{apitype|CraftingOrderRequestInfo}}
{{:Struct CraftingOrderRequestInfo|nocaption=1}}

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|C_CraftingOrders.GetCrafterOrders}} }}
{{apirow | Related Events | {{api|t=e|CRAFTINGORDERS_CAN_REQUEST}} }}
|}

==Example==
When standing at the Engineering table (Tinker's Workbench) and the Crafting Orders tab is open.
<syntaxhighlight lang="lua">
if C_TradeSkillUI.IsNearProfessionSpellFocus(Enum.Profession.Engineering) then
	local request = {
		orderType = Enum.CraftingOrderType.Public,
		searchFavorites = false,
		initialNonPublicSearch = false,
		primarySort = {
			sortType = Enum.CraftingOrderSortType.ItemName,
			reversed = false,
		},
		secondarySort = {
			sortType = Enum.CraftingOrderSortType.MaxTip,
			reversed = false,
		},
		forCrafter = true,
		offset = 0,
		profession = Enum.Profession.Engineering,
		callback = C_FunctionContainers.CreateCallback(function(result, ...)
        	print(result, ...) -- 0, 0, false, false, 0, true
			if result == Enum.CraftingOrderResult.Ok then
				local orders = C_CraftingOrders.GetCrafterOrders()
				-- do something with orders
			end
		end),
	}
	C_CraftingOrders.RequestCrafterOrders(request)
else
	print("Not at the Tinker's Workbench")
end
</syntaxhighlight>
```