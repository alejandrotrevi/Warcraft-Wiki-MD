# API GetInventoryItemsForSlot

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of items that can be equipped in a given inventory slot.
 returnTable = GetInventoryItemsForSlot(slot, returnTable [, transmogrify])

==Arguments==
:;slot:{{apitype|number}} : [[InvSlotId]] - The inventory slot ID.
:;returnTable:{{apitype|table}} - The table that will be populated with available items.
:;transmogrify:{{apitype|boolean?}}

==Returns==
:;returnTable:{{apitype|table}} - A keyvalue table [https://wowprogramming.com/docs/api_types.html#itemLocation ItemLocation bitfield] -> [[ItemLink]].

==Example==
Prints all items that can go in the main hand slot, one is currently equipped, the other is in the backpack.
<syntaxhighlight lang="lua">
/dump GetInventoryItemsForSlot(INVSLOT_MAINHAND, {})

[1]={
  [1048592]="[Dignified Headmaster's Charge]",
  [3145738]="[Recruit's Hammer of the Aurora]"
}
</syntaxhighlight>

Prints the information in a more user readable state.
<syntaxhighlight lang="lua">
local locations = {
	"player",
	"bank",
	"bags",
	"voidStorage",
	"slot",
	"bag",
	"tab",
	"voidSlot",
}

function PrintInventoryItemsForSlot(slot)
	local items = GetInventoryItemsForSlot(slot, {})
	for bitfield, link in pairs(items) do
		print(link, string.format("0x%X", bitfield))
		local locs = {EquipmentManager_UnpackLocation(bitfield)}
		local t = {}
		for k, v in pairs(locs) do
			t[locations[k]] = v or nil
		end
		DevTools_Dump(t)
	end
end

-- /run PrintInventoryItemsForSlot(INVSLOT_MAINHAND)
</syntaxhighlight>
<syntaxhighlight lang="lua">
"[Dignified Headmaster's Charge]", 0x100010
	player=true,
	slot=16

"[Recruit's Hammer of the Aurora]", 0x30000A
	player=true,
	bags=true,
	bag=0,
	slot=10
</syntaxhighlight>
```