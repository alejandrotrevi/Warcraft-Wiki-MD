# API C GossipInfo.GetOptions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Returns the available gossip options at a quest giver.
 info = C_GossipInfo.GetOptions()

==Returns==
:;info:{{apitype|GossipOptionUIInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| gossipOptionID || {{apitype|number?}} || This can be <code>nil</code> to avoid automation
|-
| name || {{apitype|string}} || Text of the gossip item
|-
| icon || {{apitype|fileID}} || Icon of the gossip type
|-
| rewards || {{apitype|GossipOptionRewardInfo[]}} || 
|-
| status || {{apitype|Enum.GossipOptionStatus}} || 
|-
| spellID || {{apitype|number?}} || 
|-
| flags || {{apitype|number}} || 
|-
| overrideIconID || {{apitype|fileID?}} || 
|-
| selectOptionWhenOnlyOption || {{apitype|boolean}} || 
|-
| orderIndex || {{apitype|number}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ GossipOptionRewardInfo
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| quantity || {{apitype|number}} || 
|-
| rewardType || {{apitype|Enum.GossipOptionRewardType}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.GossipOptionRewardType
! Value !! Field !! Description
|-
| 0 || Item || 
|-
| 1 || Currency || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.GossipOptionStatus
! Value !! Field !! Description
|-
| 0 || Available || 
|-
| 1 || Unavailable || 
|-
| 2 || Locked || 
|-
| 3 || AlreadyComplete || 
|}

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|GOSSIP_SHOW}} }}
{{apirow | Related API | {{api|C_GossipInfo.SelectOption}}<br>{{api|C_GossipInfo.SelectOptionByIndex}}<br>{{api|C_GossipInfo.SelectActiveQuest}}<br>{{api|C_GossipInfo.SelectAvailableQuest}} }}
|}

==Example==
<onlyinclude>Prints gossip options and automatically selects the vendor gossip when e.g. at an innkeeper.
<syntaxhighlight lang="lua">
local function OnEvent(self, event)
	local info = C_GossipInfo.GetOptions()
	for i, v in pairs(info) do
		print(i, v.icon, v.name, v.gossipOptionID)
		if v.icon == 132060 then -- interface/gossipframe/vendorgossipicon.blp
			print("Selecting vendor gossip option.")
			C_GossipInfo.SelectOption(v.gossipOptionID)
		end
	end
end

local f = CreateFrame("Frame")
f:RegisterEvent("GOSSIP_SHOW")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 10.0.7|note=Changed the <code>gossipOptionID</code> field to be nilable.}}
* {{Patch 10.0.0|note=Removed the <code>type</code> field (banker, battlemaster, binder, gossip, healer, petition, tabard, taxi, trainer, unlearn, vendor, workorder, chatbubble). Added <code>gossipOptionID, icon, flags, overrideIconID, selectOptionWhenOnlyOption, orderIndex</code> fields.}}
* {{Patch 9.0.2|note=Added <code>spellID</code> field.}}
* {{Patch 9.0.1|note=Namespaced to <code>C_GossipInfo.GetOptions()</code> and returns structured data.}}
* {{Patch 1.0.0|note=Added as {{api|GetGossipOptions}}()}}
```