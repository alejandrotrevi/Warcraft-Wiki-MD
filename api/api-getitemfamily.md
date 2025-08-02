# API GetItemFamily

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the bag type that an item can go into, or for bags the type of items that it can contain.
 bagType = GetItemFamily(item)

==Arguments==
:;item:{{apitype|number,string}} : {{:ItemInfo}}

==Returns==
:;bagType:{{apitype|number}} : [[ItemFamily]] - Bitfield of the type of bags an item can go into, or if the item is a container what it can contain. Will return <code>nil</code> for uncached items, like most item API.

==Example==
<onlyinclude><syntaxhighlight lang="lua">
local itemFamilyIDs = {
	[1] = "Arrows",
	[2] = "Bullets",
	[3] = "Soul Shards",
	[4] = "Leatherworking Supplies",
	[5] = "Inscription Supplies",
	[6] = "Herbs",
	[7] = "Enchanting Supplies",
	[8] = "Engineering Supplies",
	[9] = "Keys",
	[10] = "Gems",
	[11] = "Mining Supplies",
	[12] = "Soulbound Equipment",
	[13] = "Vanity Pets",
	[14] = "Currency Tokens",
	[15] = "Quest Items",
	[16] = "Fishing Supplies",
	[17] = "Cooking Supplies",
	[20] = "Toys",
	[21] = "Archaeology",
	[22] = "Alchemy",
	[23] = "Blacksmithing",
	[24] = "First Aid",
	[25] = "Jewelcrafting",
	[26] = "Skinning",
	[27] = "Tailoring",
}

local itemFamilyFlags = {}
for k, v in pairs(itemFamilyIDs) do
	itemFamilyFlags[2^(k-1)] = v
end

local function PrintItemFamily(item)
	local bagType = GetItemFamily(item)
	print(format("0x%X", bagType))
	for k, v in pairs(itemFamilyFlags) do
		if bit.band(bagType, k) > 0 then
			print(format("0x%X, %s", k, v))
		end
	end
end
</syntaxhighlight>
<syntaxhighlight lang="lua">
PrintItemFamily(22786) -- Dreaming Glory
-- 0x200020
-- 0x20, Herbs
-- 0x200000, Alchemy

PrintItemFamily(190395) -- Serevite Ore
-- 0x1400480
-- 0x80, Engineering Supplies
-- 0x400, Mining Supplies
-- 0x400000, Blacksmithing
-- 0x1000000, Jewelcrafting

PrintItemFamily(37700) -- Crystallized Air
-- 0x4004C8
-- 0x8, Leatherworking Supplies
-- 0x40, Enchanting Supplies
-- 0x80, Engineering Supplies
-- 0x400, Mining Supplies
-- 0x400000, Blacksmithing

PrintItemFamily(38347) -- Mammoth Mining Bag
-- 0x400
-- 0x400, Mining Supplies
</syntaxhighlight></onlyinclude>

==Details==
* {{:ItemFamily}}

==Patch changes==
* {{Patch 2.4.0|note=Added.}}

==See also==
*{{api|C_Container.GetContainerNumFreeSlots}} - Returns the number of free slots & the bagType that an equipped bag or backpack belongs to.
```