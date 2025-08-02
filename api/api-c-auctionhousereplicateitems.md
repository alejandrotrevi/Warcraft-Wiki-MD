# API C AuctionHouse.ReplicateItems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Queries all auctions listed on the Auction House.
 C_AuctionHouse.ReplicateItems()

==Details==
* There's a 15 min account-wide throttle between each successful {{api|C_AuctionHouse.ReplicateItems}}() call, which triggers {{api|t=e|REPLICATE_ITEM_LIST_UPDATE}}.
* Afterwards item information can be queried with {{api|C_AuctionHouse.GetReplicateItemInfo}}() which accepts an index from 0 up to {{api|C_AuctionHouse.GetNumReplicateItems}}()-1
* REPLICATE_ITEM_LIST_UPDATE will also fire for each auction item that was cached from the server after calling <code>C_AuctionHouse.GetReplicateItemInfo()</code>
* This disconnected clients on busy servers with more than 80k auctions, even with throttling.<ref>{{ref web|url=https://github.com/Auctionator/Auctionator/pull/928|author=plusmouse|date=2020-12-06|title=Remove C_AuctionHouse.ReplicateItems scan #928}}</ref> But was hotfixed during patch 9.0.2 to not include player names anymore.
*As of 2022-12-10, there seems to be a limit on how many REPLICATE_ITEM_LIST_UPDATE fire per frame, about 2000. Hence, if more {{api|C_AuctionHouse.GetReplicateItemInfo}}() calls are made recently, they'll be ignored or cause unnecessary slowdowns.

==Example==
<onlyinclude>Attempts to query the auction house when opened and loads any uncached items from the server.
<syntaxhighlight lang="lua">
local initialQuery
local auctions = {}
 
local function ScanAuctions()
	local beginTime = debugprofilestop()
	local continuables = {}
	wipe(auctions)
	for i = 0, C_AuctionHouse.GetNumReplicateItems()-1 do
		auctions[i] = {C_AuctionHouse.GetReplicateItemInfo(i)}
		if not auctions[i][18] then -- hasAllInfo
			local item = Item:CreateFromItemID(auctions[i][17]) -- itemID
			continuables[item] = true

			item:ContinueOnItemLoad(function()
				auctions[i] = {C_AuctionHouse.GetReplicateItemInfo(i)}
				continuables[item] = nil
				if not next(continuables) then
					print(format("Scanned %d auctions in %d milliseconds", #auctions+1, debugprofilestop()-beginTime))
					-- do something with `auctions` or fire some callback
				end
			end)
		end
	end
end

local function OnEvent(self, event)
	if event == "AUCTION_HOUSE_SHOW" then
		C_AuctionHouse.ReplicateItems()
		initialQuery = true
	elseif event == "REPLICATE_ITEM_LIST_UPDATE" then
		if initialQuery then
			ScanAuctions()
			initialQuery = false
		end
	end
end

local f = CreateFrame("Frame")
f:RegisterEvent("AUCTION_HOUSE_SHOW")
f:RegisterEvent("REPLICATE_ITEM_LIST_UPDATE")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight>

 > Scanned 81338 auctions in 2644 milliseconds</onlyinclude>

==Patch changes==
* {{Patch 9.0.2|note=Hotfixed <code>owner</code> and <code>ownerFullName</code> to always return nil (except for your own auctions) as that seemed to be the cause of disconnects.}}
* {{Patch 8.3.0|note=Added. Replaces performing a "getall" {{api|QueryAuctionItems}}()<ref>{{ref FrameXML|Blizzard_Deprecated/Deprecated_8_3_0.lua|8.3.0||13}}</ref>}}

==See also==
* {{api|C_AuctionHouse.SendSearchQuery}}()

==References==
{{Reflist}}

{{apinavbox|C_AuctionHouse}}
```