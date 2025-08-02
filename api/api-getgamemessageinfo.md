# API GetGameMessageInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the error message for an id.
 stringId, soundKitID, voiceID = GetGameMessageInfo(messageType)

==Arguments==
:;messageType:{{apitype|number}} - <code>errorType</code> index from {{api|t=e|UI_INFO_MESSAGE}} or {{api|t=e|UI_ERROR_MESSAGE}}

==Returns==
:;stringId:{{apitype|string}} - Name of the {{dbc|globalstrings#search=ERR_|ERR_*}} globalstring
:;soundKitID:{{apitype|number?}} - Plays a sound effect with {{api|PlaySound}}()
:;voiceID:{{apitype|number?}} - Plays a voice line (Error Speech) with {{api|PlayVocalErrorSoundID}}()

==Example==
<syntaxhighlight lang="lua">
/dump GetGameMessageInfo(365) -- "ERR_SPELL_OUT_OF_RANGE", nil, 46
</syntaxhighlight>

Prints the related Lua Enum and GlobalString.
<syntaxhighlight lang="lua">
/dump LE_GAME_ERR_SPELL_OUT_OF_RANGE -- 365
/dump ERR_SPELL_OUT_OF_RANGE -- "Out of range."
</syntaxhighlight>

==Values==
<onlyinclude>:{{icon-exclamation}}The <code>errorType</code> is an index and likely to be shifted up on every patch so it's recommended to use string (pattern) matching instead, for example:
<syntaxhighlight lang="lua">
local function OnEvent(self, event, errorType, message)
	if message == ERR_OUT_OF_RANGE then
		print(message)
	end
end

local f = CreateFrame("Frame")
f:RegisterEvent("UI_ERROR_MESSAGE")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight>


{{i-note|This list is up to date as of Patch 9.2.5 (43971) May 31 2022}}
<!-- https://github.com/Ketho/WowpediaDoc/blob/master/KethoWowpedia/scripts/GameError.lua -->
{| class="sortable darktable zebra col1-center"
! idx !! skit !! voice !! stringId !! GlobalString (enUS)
|-
| 1 ||  ||  || ERR_SYSTEM || 
|-
| 2 ||  ||  || ERR_INTERNAL_ERROR || Internal Error
|-
| 3 ||  || 0 || ERR_INV_FULL || Inventory is full.
|-
| 4 ||  ||  || ERR_BANK_FULL || Your bank is full
|-
| 5 ||  || 2 || ERR_CANT_EQUIP_LEVEL_I || You must reach level %d to use that item.
|-
| 6 ||  || 41 || ERR_CANT_EQUIP_SKILL || You aren't skilled enough to use that item.
|-
| 7 ||  || 3 || ERR_CANT_EQUIP_EVER || You can never use that item.
|-
| 8 ||  ||  || ERR_CANT_EQUIP_RANK || You don't have the required rank for that item
|-
| 9 ||  ||  || ERR_CANT_EQUIP_RATING || You don't have the personal, team, or battleground rating required to buy that item
|-
| 10 ||  ||  || ERR_CANT_EQUIP_REPUTATION || You don't have the required reputation for that item
|-
| 11 ||  || 48 || ERR_PROFICIENCY_NEEDED || You do not have the required proficiency for that item.
|-
| 12 ||  || 27 || ERR_WRONG_SLOT || That item does not go in that slot.
|-
| 13 ||  || 41 || ERR_CANT_EQUIP_NEED_TALENT || You do not have the required talent to equip that.
|-
| 14 ||  || 29 || ERR_BAG_FULL || That bag is full.
|-
| 15 ||  ||  || ERR_INTERNAL_BAG_ERROR || Internal Bag Error
|-
| 16 ||  ||  || ERR_DESTROY_NONEMPTY_BAG || You can only do that with empty bags.
|-
| 17 ||  || 26 || ERR_BAG_IN_BAG || Can't put non-empty bags in other bags.
|-
| 18 ||  ||  || ERR_TOO_MANY_SPECIAL_BAGS || You cannot equip another bag of that type
|-
| 19 ||  ||  || ERR_TRADE_EQUIPPED_BAG || You can't trade equipped bags.
|-
| 20 ||  || 28 || ERR_AMMO_ONLY || Only ammo can go there.
|-
| 21 ||  ||  || ERR_NO_SLOT_AVAILABLE || No equipment slot is available for that item.
|-
| 22 ||  ||  || ERR_WRONG_BAG_TYPE || That item doesn't go in that container.
|-
| 23 ||  || 30 || ERR_ITEM_MAX_COUNT || You can't carry any more of those items.
|-
| 24 ||  || 44 || ERR_NOT_EQUIPPABLE || This item cannot be equipped.
|-
| 25 ||  ||  || ERR_CANT_STACK || This item cannot stack.
|-
| 26 ||  ||  || ERR_CANT_SWAP || These items can't be swapped.
|-
| 27 ||  ||  || ERR_SLOT_EMPTY || That slot is empty.
|-
| 28 ||  ||  || ERR_ITEM_NOT_FOUND || The item was not found.
|-
| 29 ||  ||  || ERR_TOO_FEW_TO_SPLIT || Tried to split more than number in stack.
|-
| 30 ||  ||  || ERR_SPLIT_FAILED || Couldn't split those items.
|-
| 31 ||  || 25 || ERR_NOT_A_BAG || Not a bag.
|-
| 32 ||  ||  || ERR_NOT_OWNER || You don't own that item.
|-
| 33 ||  ||  || ERR_ONLY_ONE_QUIVER || You can only equip one quiver.
|-
| 34 ||  ||  || ERR_NO_BANK_SLOT || You must purchase that bag slot first
|-
| 35 ||  ||  || ERR_NO_BANK_HERE || You are too far away from a bank.
|-
| 36 ||  || 61 || ERR_ITEM_LOCKED || Item is locked.
|-
| 37 ||  || 42 || ERR_2HANDED_EQUIPPED || Cannot equip that with a two-handed weapon.
|-
| 38 ||  ||  || ERR_VENDOR_NOT_INTERESTED || The merchant doesn't want that item.
|-
| 39 ||  ||  || ERR_VENDOR_REFUSE_SCRAPPABLE_AZERITE || The merchant doesn't want that item. Bring it to the Scrapper to extract Titan Residuum.
|-
| 40 ||  ||  || ERR_VENDOR_HATES_YOU || That merchant doesn't like you.
|-
| 41 ||  ||  || ERR_VENDOR_SOLD_OUT || That item is currently sold out.
|-
| 42 ||  ||  || ERR_VENDOR_TOO_FAR || You are too far away.
|-
| 43 ||  ||  || ERR_VENDOR_DOESNT_BUY || You cannot sell items to this merchant
|-
| 44 ||  || 40 || ERR_NOT_ENOUGH_MONEY || You don't have enough money.
|-
| 45 || 123 ||  || ERR_RECEIVE_ITEM_S || %s received.
|-
| 46 ||  || 4 || ERR_DROP_BOUND_ITEM || You can't drop a soulbound item.
|-
| 47 ||  || 59 || ERR_TRADE_BOUND_ITEM || You can't trade a soulbound item.
|-
| 48 ||  || 59 || ERR_TRADE_QUEST_ITEM || You can't trade a quest item.
|-
| 49 ||  || 59 || ERR_TRADE_TEMP_ENCHANT_BOUND || You may not trade an item with a temporary enhancement.
|-
| 50 ||  ||  || ERR_TRADE_GROUND_ITEM || You can't trade an item from the ground.
|-
| 51 ||  ||  || ERR_TRADE_BAG || You can't trade non-empty bags.
|-
| 52 ||  ||  || ERR_TRADE_FACTION_SPECIFIC || You can't trade a faction specific item to the opposing faction
|-
| 53 ||  ||  || ERR_SPELL_FAILED_S || %s
|-
| 54 ||  || 5 || ERR_ITEM_COOLDOWN || Item is not ready yet.
|-
| 55 ||  || 47 || ERR_POTION_COOLDOWN || You can't do that yet.
|-
| 56 ||  || 7 || ERR_FOOD_COOLDOWN || You are too full to eat more now.
|-
| 57 ||  || 12 || ERR_SPELL_COOLDOWN || Spell is not ready yet.
|-
| 58 ||  || 50 || ERR_ABILITY_COOLDOWN || Ability is not ready yet.
|-
| 59 ||  || 13 || ERR_SPELL_ALREADY_KNOWN_S || You already know %s.
|-
| 60 ||  ||  || ERR_PET_SPELL_ALREADY_KNOWN_S || Your pet already knows %s.
|-
| 61 ||  ||  || ERR_PROFICIENCY_GAINED_S || You have gained %s proficiency.
|-
| 62 ||  ||  || ERR_SKILL_GAINED_S || You have gained the %s skill.
|-
| 63 ||  ||  || ERR_SKILL_UP_SI || Your skill in %s has increased to %d.
|-
| 64 ||  ||  || ERR_LEARN_SPELL_S || You have learned a new spell: %s.
|-
| 65 ||  ||  || ERR_LEARN_ABILITY_S || You have learned a new ability: %s.
|-
| 66 ||  ||  || ERR_LEARN_PASSIVE_S || You have learned a new passive effect: %s.
|-
| 67 ||  ||  || ERR_LEARN_RECIPE_S || You have learned how to create a new item: %s.
|-
| 68 ||  ||  || ERR_LEARN_COMPANION_S || You have added the pet %s to your collection.
|-
| 69 ||  ||  || ERR_LEARN_MOUNT_S || You have added the mount %s to your collection.
|-
| 70 ||  ||  || ERR_LEARN_TOY_S || %s has been added to your Toy Box.
|-
| 71 ||  ||  || ERR_LEARN_HEIRLOOM_S || %s has been added to your heirloom collection.
|-
| 72 ||  ||  || ERR_LEARN_TRANSMOG_S || %s has been added to your appearance collection.
|-
| 73 ||  ||  || ERR_COMPLETED_TRANSMOG_SET_S || You've completed the set %s.
|-
| 74 ||  ||  || ERR_APPEARANCE_ALREADY_LEARNED || You already have that appearance
|-
| 75 ||  ||  || ERR_REVOKE_TRANSMOG_S || %s has been removed from your appearance collection.
|-
| 76 ||  ||  || ERR_INVITE_PLAYER_S || You have invited %s to join your group.
|-
| 77 ||  ||  || ERR_INVITE_SELF || You can't invite yourself to a group.
|-
| 78 ||  ||  || ERR_INVITED_TO_GROUP_SS || [%s] has invited you to join a group.
|-
| 79 ||  || 20 || ERR_INVITED_ALREADY_IN_GROUP_SS || [%s] invited you to a group, but you could not accept because you are already in a group.
|-
| 80 ||  || 20 || ERR_ALREADY_IN_GROUP_S || %s is already in a group.
|-
| 81 ||  ||  || ERR_CROSS_REALM_RAID_INVITE || You can't invite a player from another realm to a raid group.
|-
| 82 ||  ||  || ERR_PLAYER_BUSY_S || %s is busy right now.
|-
| 83 ||  ||  || ERR_NEW_LEADER_S || %s is now the group leader.
|-
| 84 ||  ||  || ERR_NEW_LEADER_YOU || You are now the group leader.
|-
| 85 ||  ||  || ERR_NEW_GUIDE_S || %s is now the Dungeon Guide.
|-
| 86 ||  ||  || ERR_NEW_GUIDE_YOU || You are now the Dungeon Guide.
|-
| 87 ||  ||  || ERR_LEFT_GROUP_S || %s leaves the party.
|-
| 88 ||  ||  || ERR_LEFT_GROUP_YOU || You leave the group.
|-
| 89 ||  ||  || ERR_GROUP_DISBANDED || Your group has been disbanded.
|-
| 90 || 882 ||  || ERR_DECLINE_GROUP_S || %s declines your group invitation.
|-
| 91 ||  ||  || ERR_JOINED_GROUP_S || %s joins the party.
|-
| 92 ||  ||  || ERR_UNINVITE_YOU || You have been removed from the group.
|-
| 93 ||  ||  || ERR_BAD_PLAYER_NAME_S || Cannot find player '%s'.
|-
| 94 ||  ||  || ERR_NOT_IN_GROUP || You aren't in a party.
|-
| 95 ||  ||  || ERR_TARGET_NOT_IN_GROUP_S || %s is not in your party.
|-
| 96 ||  ||  || ERR_TARGET_NOT_IN_INSTANCE_S || %s is not in your instance.
|-
| 97 ||  ||  || ERR_NOT_IN_INSTANCE_GROUP || You aren't in an instance group.
|-
| 98 ||  || 8 || ERR_GROUP_FULL || Your party is full.
|-
| 99 ||  ||  || ERR_NOT_LEADER || You are not the party leader.
|-
| 100 ||  ||  || ERR_PLAYER_DIED_S || %s has died.
|-
| 101 || 888 ||  || ERR_GUILD_CREATE_S || %s created.
|-
| 102 ||  ||  || ERR_GUILD_INVITE_S || You have invited %s to join your guild.
|-
| 103 || 888 ||  || ERR_INVITED_TO_GUILD_SSS || [%s] invites you to join %s.
|-
| 104 ||  ||  || ERR_ALREADY_IN_GUILD_S || %s is already in a guild.
|-
| 105 ||  ||  || ERR_ALREADY_INVITED_TO_GUILD_S || %s has already been invited to a guild.
|-
| 106 ||  ||  || ERR_INVITED_TO_GUILD || You have already been invited into a guild.
|-
| 107 ||  ||  || ERR_ALREADY_IN_GUILD || You are already in a guild.
|-
| 108 ||  ||  || ERR_GUILD_ACCEPT || You have joined the guild.
|-
| 109 ||  ||  || ERR_GUILD_DECLINE_S || %s declines your guild invitation.
|-
| 110 ||  ||  || ERR_GUILD_DECLINE_AUTO_S || %s is declining all guild invitations.
|-
| 111 ||  || 62 || ERR_GUILD_PERMISSIONS || You don't have permission to do that.
|-
| 112 ||  ||  || ERR_GUILD_JOIN_S || %s has joined the guild.
|-
| 113 ||  ||  || ERR_GUILD_FOUNDER_S || Congratulations, you are a founding member of %s!
|-
| 114 ||  ||  || ERR_GUILD_PROMOTE_SSS || %s has promoted %s to %s.
|-
| 115 ||  ||  || ERR_GUILD_DEMOTE_SS || %s  has been demoted to %s.
|-
| 116 ||  ||  || ERR_GUILD_DEMOTE_SSS || %s has demoted %s to %s.
|-
| 117 ||  ||  || ERR_GUILD_INVITE_SELF || You can't invite yourself to a guild.
|-
| 118 ||  ||  || ERR_GUILD_QUIT_S || You are no longer a member of %s.
|-
| 119 ||  ||  || ERR_GUILD_LEAVE_S || %s has left the guild.
|-
| 120 ||  ||  || ERR_GUILD_REMOVE_SS || %s has been kicked out of the guild by %s.
|-
| 121 ||  ||  || ERR_GUILD_REMOVE_SELF || You have been kicked out of the guild.
|-
| 122 ||  ||  || ERR_GUILD_DISBAND_S || %s has disbanded the guild.
|-
| 123 ||  ||  || ERR_GUILD_DISBAND_SELF || You have disbanded the guild.
|-
| 124 ||  ||  || ERR_GUILD_LEADER_S || %s has been promoted to Guild Master.
|-
| 125 ||  ||  || ERR_GUILD_LEADER_SELF || You are now the Guild Master.
|-
| 126 ||  ||  || ERR_GUILD_PLAYER_NOT_FOUND_S || "%s" not found.
|-
| 127 ||  ||  || ERR_GUILD_PLAYER_NOT_IN_GUILD_S || %s is not in your guild.
|-
| 128 ||  ||  || ERR_GUILD_PLAYER_NOT_IN_GUILD || You are not in a guild.
|-
| 129 ||  ||  || ERR_GUILD_CANT_PROMOTE_S || 
|-
| 130 ||  ||  || ERR_GUILD_CANT_DEMOTE_S || 
|-
| 131 ||  ||  || ERR_GUILD_NOT_IN_A_GUILD || 
|-
| 132 ||  ||  || ERR_GUILD_INTERNAL || Internal guild error.
|-
| 133 ||  ||  || ERR_GUILD_LEADER_IS_S || %s is the leader of your guild.
|-
| 134 ||  ||  || ERR_GUILD_LEADER_CHANGED_SS || %s has made %s the new Guild Master.
|-
| 135 ||  ||  || ERR_GUILD_DISBANDED || Guild has been disbanded.
|-
| 136 ||  ||  || ERR_GUILD_NOT_ALLIED || You cannot invite players from the opposing alliance
|-
| 137 ||  ||  || ERR_GUILD_LEADER_LEAVE || You must promote a new Guild Master using /gleader before leaving the guild.
|-
| 138 ||  ||  || ERR_GUILD_RANKS_LOCKED || Temporary guild error.  Please try again!
|-
| 139 ||  ||  || ERR_GUILD_RANK_IN_USE || That guild rank is currently in use.
|-
| 140 ||  ||  || ERR_GUILD_RANK_TOO_HIGH_S || %s's rank is too high
|-
| 141 ||  ||  || ERR_GUILD_RANK_TOO_LOW_S || %s is already at the lowest rank
|-
| 142 ||  ||  || ERR_GUILD_NAME_EXISTS_S || There is already a guild named "%s".
|-
| 143 ||  ||  || ERR_GUILD_WITHDRAW_LIMIT || You cannot withdraw that much from the guild bank.
|-
| 144 ||  ||  || ERR_GUILD_NOT_ENOUGH_MONEY || The guild bank does not have enough money
|-
| 145 ||  ||  || ERR_GUILD_TOO_MUCH_MONEY || The guild bank is at gold limit
|-
| 146 ||  ||  || ERR_GUILD_BANK_CONJURED_ITEM || You cannot store conjured items in the guild bank
|-
| 147 ||  ||  || ERR_GUILD_BANK_EQUIPPED_ITEM || You must unequip that item first
|-
| 148 ||  ||  || ERR_GUILD_BANK_BOUND_ITEM || You cannot store soulbound items in the guild bank
|-
| 149 ||  ||  || ERR_GUILD_BANK_QUEST_ITEM || You cannot store quest items in the guild bank
|-
| 150 ||  ||  || ERR_GUILD_BANK_WRAPPED_ITEM || You cannot store wrapped items in the guild bank
|-
| 151 ||  ||  || ERR_GUILD_BANK_FULL || This guild bank tab is full
|-
| 152 ||  ||  || ERR_GUILD_BANK_WRONG_TAB || Incorrect bank tab
|-
| 153 ||  ||  || ERR_NO_GUILD_CHARTER || You don't have a guild charter.
|-
| 154 ||  || 10 || ERR_OUT_OF_RANGE || Out of range.
|-
| 155 ||  ||  || ERR_PLAYER_DEAD || You can't do that when you're dead.
|-
| 156 ||  ||  || ERR_CLIENT_LOCKED_OUT || You can't do that right now.
|-
| 157 ||  ||  || ERR_CLIENT_ON_TRANSPORT || You can't do that while on a vehicle or transport.
|-
| 158 ||  ||  || ERR_KILLED_BY_S || %s has slain you.
|-
| 159 ||  || 33 || ERR_LOOT_LOCKED || Someone is already looting that corpse.
|-
| 160 ||  || 35 || ERR_LOOT_TOO_FAR || You are too far away to loot that corpse.
|-
| 161 ||  || 31 || ERR_LOOT_DIDNT_KILL || You don't have permission to loot that corpse.
|-
| 162 ||  || 32 || ERR_LOOT_BAD_FACING || You must be facing the corpse to loot it.
|-
| 163 ||  ||  || ERR_LOOT_NOTSTANDING || You need to be standing up to loot something!
|-
| 164 ||  ||  || ERR_LOOT_STUNNED || You can't loot anything while stunned!
|-
| 165 ||  ||  || ERR_LOOT_NO_UI || You can't loot right now.
|-
| 166 ||  ||  || ERR_LOOT_WHILE_INVULNERABLE || Cannot loot while invulnerable.
|-
| 167 ||  ||  || ERR_NO_LOOT || There is no loot.
|-
| 168 ||  ||  || ERR_QUEST_ACCEPTED_S || Quest accepted: %s
|-
| 169 ||  ||  || ERR_QUEST_COMPLETE_S || %s completed.
|-
| 170 || 847 ||  || ERR_QUEST_FAILED_S || %s failed.
|-
| 171 || 847 ||  || ERR_QUEST_FAILED_BAG_FULL_S || %s failed: Inventory is full.
|-
| 172 || 847 ||  || ERR_QUEST_FAILED_MAX_COUNT_S || Turn in for "%s" failed. This quest's unique reward already exists in your inventory. Remove it to complete this quest.
|-
| 173 || 847 ||  || ERR_QUEST_FAILED_LOW_LEVEL || You are not high enough level for that quest.
|-
| 174 || 847 ||  || ERR_QUEST_FAILED_MISSING_ITEMS || You don't have the required items with you.  Check storage.
|-
| 175 || 847 ||  || ERR_QUEST_FAILED_WRONG_RACE || That quest is not available to your race.
|-
| 176 || 847 ||  || ERR_QUEST_FAILED_NOT_ENOUGH_MONEY || You don't have enough money for that quest.
|-
| 177 || 847 ||  || ERR_QUEST_FAILED_EXPANSION || This quest requires an expansion enabled account.
|-
| 178 || 847 ||  || ERR_QUEST_ONLY_ONE_TIMED || You can only be on one timed quest at a time
|-
| 179 || 847 ||  || ERR_QUEST_NEED_PREREQS || You don't meet the requirements for that quest.
|-
| 180 || 847 ||  || ERR_QUEST_NEED_PREREQS_CUSTOM || %s
|-
| 181 || 847 ||  || ERR_QUEST_ALREADY_ON || You are already on that quest.
|-
| 182 || 847 ||  || ERR_QUEST_ALREADY_DONE || You have completed that quest.
|-
| 183 || 847 ||  || ERR_QUEST_ALREADY_DONE_DAILY || You have completed that daily quest today.
|-
| 184 || 847 ||  || ERR_QUEST_HAS_IN_PROGRESS || Progress Bar objective not completed
|-
| 185 ||  ||  || ERR_QUEST_REWARD_EXP_I || Experience gained: %d.
|-
| 186 ||  ||  || ERR_QUEST_REWARD_MONEY_S || Received %s.
|-
| 187 || 847 ||  || ERR_QUEST_MUST_CHOOSE || You must choose a reward.
|-
| 188 || 847 ||  || ERR_QUEST_LOG_FULL || Your quest log is full.
|-
| 189 ||  ||  || ERR_COMBAT_DAMAGE_SSI || %s hits %s for %d damage!
|-
| 190 ||  ||  || ERR_INSPECT_S || %s is inspecting you.
|-
| 191 ||  || 51 || ERR_CANT_USE_ITEM || You can't use that item.
|-
| 192 ||  || 51 || ERR_CANT_USE_ITEM_IN_ARENA || You can't use that item in an arena.
|-
| 193 ||  || 51 || ERR_CANT_USE_ITEM_IN_RATED_BATTLEGROUND || You can't use that item in a rated battleground.
|-
| 194 ||  || 49 || ERR_MUST_EQUIP_ITEM || You must equip that item to use it.
|-
| 195 ||  ||  || ERR_PASSIVE_ABILITY || You can't put a passive ability in the action bar.
|-
| 196 ||  || 43 || ERR_2HSKILLNOTFOUND || You cannot dual-wield
|-
| 197 ||  || 38 || ERR_NO_ATTACK_TARGET || There is nothing to attack.
|-
| 198 ||  || 11 || ERR_INVALID_ATTACK_TARGET || You cannot attack that target.
|-
| 199 ||  ||  || ERR_ATTACK_PVP_TARGET_WHILE_UNFLAGGED || You cannot do that to a PVP target while PVP is disabled.
|-
| 200 ||  ||  || ERR_ATTACK_STUNNED || Can't attack while stunned.
|-
| 201 ||  ||  || ERR_ATTACK_PACIFIED || Can't attack while pacified.
|-
| 202 ||  ||  || ERR_ATTACK_MOUNTED || Can't attack while mounted.
|-
| 203 ||  ||  || ERR_ATTACK_FLEEING || Can't attack while fleeing.
|-
| 204 ||  ||  || ERR_ATTACK_CONFUSED || Can't attack while confused.
|-
| 205 ||  ||  || ERR_ATTACK_CHARMED || Can't attack while charmed.
|-
| 206 ||  ||  || ERR_ATTACK_DEAD || Can't attack while dead.
|-
| 207 ||  ||  || ERR_ATTACK_PREVENTED_BY_MECHANIC_S || Can't attack while %s.
|-
| 208 ||  ||  || ERR_ATTACK_CHANNEL || Can't attack while channeling.
|-
| 209 ||  ||  || ERR_TAXISAMENODE || You are already there!
|-
| 210 ||  ||  || ERR_TAXINOSUCHPATH || There is no direct path to that destination!
|-
| 211 ||  ||  || ERR_TAXIUNSPECIFIEDSERVERERROR || UNSPECIFIED TAXI SERVER ERROR
|-
| 212 ||  || 54 || ERR_TAXINOTENOUGHMONEY || You don't have enough money!
|-
| 213 ||  ||  || ERR_TAXITOOFARAWAY || You are too far away from the taxi stand!
|-
| 214 ||  ||  || ERR_TAXINOVENDORNEARBY || There is no taxi vendor nearby!
|-
| 215 ||  ||  || ERR_TAXINOTVISITED || You haven't reached that flight location on foot yet!
|-
| 216 ||  ||  || ERR_TAXIPLAYERBUSY || You are busy and can't use the taxi service now.
|-
| 217 ||  ||  || ERR_TAXIPLAYERALREADYMOUNTED || You are already mounted! Dismount first.
|-
| 218 ||  ||  || ERR_TAXIPLAYERSHAPESHIFTED || You can't take a taxi while shapeshifted!
|-
| 219 ||  ||  || ERR_TAXIPLAYERMOVING || You are moving.
|-
| 220 ||  ||  || ERR_TAXINOPATHS || You don't know any locations connected to this one.
|-
| 221 ||  ||  || ERR_TAXINOTELIGIBLE || You cannot use this taxi currently.
|-
| 222 ||  ||  || ERR_TAXINOTSTANDING || You need to be standing to go anywhere.
|-
| 223 ||  ||  || ERR_NO_REPLY_TARGET || You have nobody to reply to yet.
|-
| 224 ||  || 45 || ERR_GENERIC_NO_TARGET || You have no target.
|-
| 225 ||  ||  || ERR_INITIATE_TRADE_S || You have requested to trade with %s.
|-
| 226 || 888 ||  || ERR_TRADE_REQUEST_S || %s has requested to trade with you.
|-
| 227 ||  ||  || ERR_TRADE_BLOCKED_S || %s has requested to trade.  You have refused.
|-
| 228 ||  ||  || ERR_TRADE_TARGET_DEAD || You can't trade with dead players.
|-
| 229 ||  ||  || ERR_TRADE_TOO_FAR || Trade target is too far away.
|-
| 230 ||  ||  || ERR_TRADE_CANCELLED || Trade canceled.
|-
| 231 ||  ||  || ERR_TRADE_COMPLETE || Trade complete.
|-
| 232 ||  ||  || ERR_TRADE_BAG_FULL || Trade failed, you don't have enough space.
|-
| 233 ||  ||  || ERR_TRADE_TARGET_BAG_FULL || Trade failed, target doesn't have enough space.
|-
| 234 ||  ||  || ERR_TRADE_MAX_COUNT_EXCEEDED || You have too many of a unique item.
|-
| 235 ||  ||  || ERR_TRADE_TARGET_MAX_COUNT_EXCEEDED || Your trade partner has too many of a unique item.
|-
| 236 ||  ||  || ERR_INVENTORY_TRADE_TOO_MANY_UNIQUE_ITEM || Your inventory would contain too many of a unique item.
|-
| 237 ||  ||  || ERR_ALREADY_TRADING || You are already trading
|-
| 238 ||  ||  || ERR_MOUNT_INVALIDMOUNTEE || You can't mount that unit.
|-
| 239 ||  ||  || ERR_MOUNT_TOOFARAWAY || That mount is too far away.
|-
| 240 ||  ||  || ERR_MOUNT_ALREADYMOUNTED || You're already mounted.
|-
| 241 ||  ||  || ERR_MOUNT_NOTMOUNTABLE || That unit can't be mounted.
|-
| 242 ||  ||  || ERR_MOUNT_NOTYOURPET || That mount isn't your pet!
|-
| 243 ||  ||  || ERR_MOUNT_OTHER || UNKNOWN MOUNT ERROR
|-
| 244 ||  ||  || ERR_MOUNT_LOOTING || You can't mount while looting!
|-
| 245 ||  ||  || ERR_MOUNT_RACECANTMOUNT || You can't mount because of your race.
|-
| 246 ||  ||  || ERR_MOUNT_SHAPESHIFTED || You can't mount while shapeshifted.
|-
| 247 ||  ||  || ERR_MOUNT_NO_FAVORITES || You have no valid favorite mounts.
|-
| 248 ||  ||  || ERR_MOUNT_NO_MOUNTS || You have no valid mounts.
|-
| 249 ||  ||  || ERR_DISMOUNT_NOPET || INTERNAL ERROR, YOU DON'T HAVE A PET TO DISMOUNT
|-
| 250 ||  ||  || ERR_DISMOUNT_NOTMOUNTED || You're not mounted!
|-
| 251 ||  ||  || ERR_DISMOUNT_NOTYOURPET || INTERNAL ERROR, DISMOUNTING A NON-PET
|-
| 252 ||  ||  || ERR_SPELL_FAILED_TOTEMS || %s
|-
| 253 ||  ||  || ERR_SPELL_FAILED_REAGENTS || %s
|-
| 254 ||  ||  || ERR_SPELL_FAILED_REAGENTS_GENERIC || Missing reagent
|-
| 255 ||  ||  || ERR_SPELL_FAILED_OPTIONAL_REAGENTS || %s
|-
| 256 ||  ||  || ERR_CANT_TRADE_GOLD || Gold may only be offered by one trader.
|-
| 257 ||  ||  || ERR_SPELL_FAILED_EQUIPPED_ITEM || Must have the proper item equipped
|-
| 258 ||  ||  || ERR_SPELL_FAILED_EQUIPPED_ITEM_CLASS_S || %s
|-
| 259 ||  ||  || ERR_SPELL_FAILED_SHAPESHIFT_FORM_S || %s
|-
| 260 ||  ||  || ERR_SPELL_FAILED_ANOTHER_IN_PROGRESS || Another action is in progress
|-
| 261 ||  ||  || ERR_BADATTACKFACING || You are facing the wrong way!
|-
| 262 ||  ||  || ERR_BADATTACKPOS || You are too far away!
|-
| 263 ||  || 52 || ERR_CHEST_IN_USE || That is already being used.
|-
| 264 ||  ||  || ERR_USE_CANT_OPEN || You can't open that.
|-
| 265 ||  || 61 || ERR_USE_LOCKED || Item is locked.
|-
| 266 ||  || 61 || ERR_DOOR_LOCKED || The door is locked.
|-
| 267 ||  || 61 || ERR_BUTTON_LOCKED || That has already been used.
|-
| 268 ||  ||  || ERR_USE_LOCKED_WITH_ITEM_S || Requires %s
|-
| 269 ||  ||  || ERR_USE_LOCKED_WITH_SPELL_S || Requires %s
|-
| 270 ||  ||  || ERR_USE_LOCKED_WITH_SPELL_KNOWN_SI || Requires %s %d
|-
| 271 ||  || 57 || ERR_USE_TOO_FAR || You are too far away.
|-
| 272 ||  ||  || ERR_USE_BAD_ANGLE || You aren't facing the right angle!
|-
| 273 ||  ||  || ERR_USE_OBJECT_MOVING || Object is in motion.
|-
| 274 ||  ||  || ERR_USE_SPELL_FOCUS || Object is a spell focus.
|-
| 275 ||  ||  || ERR_USE_DESTROYED || That is destroyed.
|-
| 276 ||  ||  || ERR_SET_LOOT_FREEFORALL || Looting set to Free for All.
|-
| 277 ||  ||  || ERR_SET_LOOT_ROUNDROBIN || Looting set to Round Robin.
|-
| 278 ||  ||  || ERR_SET_LOOT_MASTER || Looting set to Master Looter.
|-
| 279 ||  ||  || ERR_SET_LOOT_GROUP || Looting set to Group Loot.
|-
| 280 ||  ||  || ERR_SET_LOOT_THRESHOLD_S || Loot threshold set to %s.
|-
| 281 ||  ||  || ERR_NEW_LOOT_MASTER_S || %s is now the loot master.
|-
| 282 ||  ||  || ERR_SPECIFY_MASTER_LOOTER || You must specify a loot master.
|-
| 283 ||  ||  || ERR_LOOT_SPEC_CHANGED_S || Loot Specialization set to: %s
|-
| 284 ||  ||  || ERR_TAME_FAILED || %s.
|-
| 285 ||  ||  || ERR_CHAT_WHILE_DEAD || You can't chat when you're dead!
|-
| 286 ||  ||  || ERR_CHAT_PLAYER_NOT_FOUND_S || No player named '%s' is currently playing.
|-
| 287 || 1519 ||  || ERR_NEWTAXIPATH || New location discovered!
|-
| 288 ||  ||  || ERR_NO_PET || You don't have a pet!
|-
| 289 ||  ||  || ERR_NOTYOURPET || That is not your pet!
|-
| 290 ||  ||  || ERR_PET_NOT_RENAMEABLE || Your pet can't be renamed.
|-
| 291 ||  ||  || ERR_QUEST_OBJECTIVE_COMPLETE_S || %s (Complete)
|-
| 292 ||  ||  || ERR_QUEST_UNKNOWN_COMPLETE || Objective Complete.
|-
| 293 ||  ||  || ERR_QUEST_ADD_KILL_SII || %s slain: %d/%d
|-
| 294 ||  ||  || ERR_QUEST_ADD_FOUND_SII || %s: %d/%d
|-
| 295 ||  ||  || ERR_QUEST_ADD_ITEM_SII || %s: %d/%d
|-
| 296 ||  ||  || ERR_QUEST_ADD_PLAYER_KILL_SII || Players slain: %d/%d
|-
| 297 ||  ||  || ERR_CANNOTCREATEDIRECTORY || Cannot create directory %s.
|-
| 298 ||  ||  || ERR_CANNOTCREATEFILE || Cannot create file %s.
|-
| 299 ||  ||  || ERR_PLAYER_WRONG_FACTION || Target is unfriendly.
|-
| 300 ||  ||  || ERR_PLAYER_IS_NEUTRAL || Target has not selected a faction.
|-
| 301 ||  ||  || ERR_BANKSLOT_FAILED_TOO_MANY || You've reached your limit of bag slots!
|-
| 302 ||  || 22 || ERR_BANKSLOT_INSUFFICIENT_FUNDS || You can't afford that.
|-
| 303 ||  ||  || ERR_BANKSLOT_NOTBANKER || That unit is not a banker!
|-
| 304 ||  ||  || ERR_FRIEND_DB_ERROR || Friend lookup database error.
|-
| 305 ||  ||  || ERR_FRIEND_LIST_FULL || You don't have room for any more friends.
|-
| 306 ||  ||  || ERR_FRIEND_ADDED_S || %s added to friends.
|-
| 307 ||  ||  || ERR_BATTLETAG_FRIEND_ADDED_S || 
|-
| 308 || 3332 ||  || ERR_FRIEND_ONLINE_SS || [%s] has come online.
|-
| 309 ||  ||  || ERR_FRIEND_OFFLINE_S || %s has gone offline.
|-
| 310 ||  ||  || ERR_FRIEND_NOT_FOUND || Player not found.
|-
| 311 ||  ||  || ERR_FRIEND_WRONG_FACTION || Friends must be part of your alliance.
|-
| 312 ||  ||  || ERR_FRIEND_REMOVED_S || %s removed from friends list.
|-
| 313 ||  ||  || ERR_BATTLETAG_FRIEND_REMOVED_S || 
|-
| 314 ||  ||  || ERR_FRIEND_ERROR || Unknown friend response from server.
|-
| 315 ||  ||  || ERR_FRIEND_ALREADY_S || %s is already your friend.
|-
| 316 ||  ||  || ERR_FRIEND_SELF || You can't put yourself on your friend list.
|-
| 317 ||  ||  || ERR_FRIEND_DELETED || Friend removed because the character no longer exists.
|-
| 318 ||  ||  || ERR_IGNORE_FULL || You can't ignore any more players.
|-
| 319 ||  ||  || ERR_IGNORE_SELF || You can't ignore yourself.
|-
| 320 ||  ||  || ERR_IGNORE_NOT_FOUND || Player not found.
|-
| 321 ||  ||  || ERR_IGNORE_ALREADY_S || %s is already being ignored.
|-
| 322 ||  ||  || ERR_IGNORE_ADDED_S || %s is now being ignored.
|-
| 323 ||  ||  || ERR_IGNORE_REMOVED_S || %s is no longer being ignored.
|-
| 324 ||  ||  || ERR_IGNORE_AMBIGUOUS || That name is ambiguous, type more of the player's server name
|-
| 325 ||  ||  || ERR_IGNORE_DELETED || Ignore removed because the character no longer exists.
|-
| 326 ||  ||  || ERR_ONLY_ONE_BOLT || You can only equip one quiver.
|-
| 327 ||  ||  || ERR_ONLY_ONE_AMMO || You can only equip one ammo pouch.
|-
| 328 ||  ||  || ERR_SPELL_FAILED_EQUIPPED_SPECIFIC_ITEM || 
|-
| 329 ||  || 28 || ERR_WRONG_BAG_TYPE_SUBCLASS || Only %s can be placed in that.
|-
| 330 ||  ||  || ERR_CANT_WRAP_STACKABLE || Stackable items can't be wrapped.
|-
| 331 ||  ||  || ERR_CANT_WRAP_EQUIPPED || Equipped items can't be wrapped.
|-
| 332 ||  ||  || ERR_CANT_WRAP_WRAPPED || Wrapped items can't be wrapped.
|-
| 333 ||  ||  || ERR_CANT_WRAP_BOUND || Bound items can't be wrapped.
|-
| 334 ||  ||  || ERR_CANT_WRAP_UNIQUE || Unique items can't be wrapped.
|-
| 335 ||  ||  || ERR_CANT_WRAP_BAGS || Bags can't be wrapped.
|-
| 336 ||  || 15 || ERR_OUT_OF_MANA || Not enough mana
|-
| 337 ||  || 63 || ERR_OUT_OF_RAGE || Not enough rage
|-
| 338 ||  ||  || ERR_OUT_OF_FOCUS || Not enough focus
|-
| 339 ||  || 64 || ERR_OUT_OF_ENERGY || Not enough energy
|-
| 340 ||  ||  || ERR_OUT_OF_CHI || Not enough chi
|-
| 341 ||  ||  || ERR_OUT_OF_HEALTH || Not enough health
|-
| 342 ||  ||  || ERR_OUT_OF_RUNES || Not enough runes
|-
| 343 ||  ||  || ERR_OUT_OF_RUNIC_POWER || Not enough runic power
|-
| 344 ||  ||  || ERR_OUT_OF_SOUL_SHARDS || Not enough soul shards
|-
| 345 ||  ||  || ERR_OUT_OF_LUNAR_POWER || 
|-
| 346 ||  ||  || ERR_OUT_OF_HOLY_POWER || Not enough holy power
|-
| 347 ||  ||  || ERR_OUT_OF_MAELSTROM || Not enough maelstrom
|-
| 348 ||  ||  || ERR_OUT_OF_COMBO_POINTS || That ability requires combo points
|-
| 349 ||  ||  || ERR_OUT_OF_INSANITY || Not enough insanity
|-
| 350 ||  ||  || ERR_OUT_OF_ARCANE_CHARGES || Not enough arcane charges
|-
| 351 ||  ||  || ERR_OUT_OF_FURY || Not enough fury
|-
| 352 ||  ||  || ERR_OUT_OF_PAIN || Not enough pain
|-
| 353 ||  ||  || ERR_OUT_OF_POWER_DISPLAY || Not enough %s
|-
| 354 ||  ||  || ERR_LOOT_GONE || Already looted (%d/%d)
|-
| 355 ||  ||  || ERR_MOUNT_FORCEDDISMOUNT || You dismount before continuing.
|-
| 356 ||  ||  || ERR_AUTOFOLLOW_TOO_FAR || Target is too far away.
|-
| 357 ||  ||  || ERR_UNIT_NOT_FOUND || Unknown unit.
|-
| 358 ||  ||  || ERR_INVALID_FOLLOW_TARGET || You can't follow that unit.
|-
| 359 ||  ||  || ERR_INVALID_FOLLOW_PVP_COMBAT || You can't use follow while engaged in PVP combat.
|-
| 360 ||  ||  || ERR_INVALID_FOLLOW_TARGET_PVP_COMBAT || You can't follow a player who is engaged in PVP combat.
|-
| 361 ||  ||  || ERR_INVALID_INSPECT_TARGET || You can't inspect that unit.
|-
| 362 ||  ||  || ERR_GUILDEMBLEM_SUCCESS || Guild Emblem saved.
|-
| 363 ||  ||  || ERR_GUILDEMBLEM_INVALID_TABARD_COLORS || Invalid Guild Emblem colors.
|-
| 364 ||  ||  || ERR_GUILDEMBLEM_NOGUILD || You are not part of a guild!
|-
| 365 ||  ||  || ERR_GUILDEMBLEM_NOTGUILDMASTER || Only guild leaders can create emblems.
|-
| 366 ||  || 40 || ERR_GUILDEMBLEM_NOTENOUGHMONEY || You can't afford to do that.
|-
| 367 ||  ||  || ERR_GUILDEMBLEM_INVALIDVENDOR || That's not an emblem vendor!
|-
| 368 ||  ||  || ERR_EMBLEMERROR_NOTABARDGEOSET || Change back to your normal form first!
|-
| 369 ||  || 46 || ERR_SPELL_OUT_OF_RANGE || Out of range.
|-
| 370 ||  ||  || ERR_COMMAND_NEEDS_TARGET || You must specify a target: /<command> <target's name>
|-
| 371 ||  || 1 || ERR_NOAMMO_S || %s
|-
| 372 ||  ||  || ERR_TOOBUSYTOFOLLOW || You're too busy to follow anything!
|-
| 373 || 123515 ||  || ERR_DUEL_REQUESTED || You have requested a duel.
|-
| 374 ||  ||  || ERR_DUEL_CANCELLED || Duel canceled.
|-
| 375 ||  ||  || ERR_DEATHBINDALREADYBOUND || You are already bound here!
|-
| 376 ||  ||  || ERR_DEATHBIND_SUCCESS_S || %s is now your home.
|-
| 377 ||  ||  || ERR_NOEMOTEWHILERUNNING || You can't do that while moving!
|-
| 378 ||  ||  || ERR_ZONE_EXPLORED || Discovered: %s
|-
| 379 ||  ||  || ERR_ZONE_EXPLORED_XP || Discovered %s: %d experience gained
|-
| 380 ||  || 51 || ERR_INVALID_ITEM_TARGET || That item is not a valid target.
|-
| 381 ||  ||  || ERR_INVALID_QUEST_TARGET || That quest is not a valid target.
|-
| 382 ||  ||  || ERR_IGNORING_YOU_S || %s is ignoring you.
|-
| 383 ||  ||  || ERR_FISH_NOT_HOOKED || No fish are hooked.
|-
| 384 ||  ||  || ERR_FISH_ESCAPED || Your fish got away!
|-
| 385 ||  ||  || ERR_SPELL_FAILED_NOTUNSHEATHED || You have to be unsheathed to do that!
|-
| 386 ||  ||  || ERR_PETITION_OFFERED_S || You have requested %s's signature.
|-
| 387 || 881 ||  || ERR_PETITION_SIGNED || Charter signed.
|-
| 388 || 881 ||  || ERR_PETITION_SIGNED_S || %s has signed your charter.
|-
| 389 || 882 ||  || ERR_PETITION_DECLINED_S || %s has declined to sign your petition.
|-
| 390 || 882 ||  || ERR_PETITION_ALREADY_SIGNED || You have already signed that charter.
|-
| 391 || 882 ||  || ERR_PETITION_RESTRICTED_ACCOUNT_TRIAL || Free Trial accounts may not sign guild charters. [Click To Upgrade]
|-
| 392 || 882 ||  || ERR_PETITION_ALREADY_SIGNED_OTHER || You've already signed another guild charter
|-
| 393 || 882 ||  || ERR_PETITION_IN_GUILD || You are already in a guild.
|-
| 394 || 882 ||  || ERR_PETITION_CREATOR || You can't sign your own charter.
|-
| 395 || 882 ||  || ERR_PETITION_NOT_ENOUGH_SIGNATURES || You need more signatures.
|-
| 396 || 882 ||  || ERR_PETITION_NOT_SAME_SERVER || That player is not from your server
|-
| 397 || 882 ||  || ERR_PETITION_FULL || That petition is full
|-
| 398 ||  ||  || ERR_PETITION_ALREADY_SIGNED_BY_S || %s has already signed your charter.
|-
| 399 || 882 ||  || ERR_GUILD_NAME_INVALID || Invalid guild name.
|-
| 400 ||  ||  || ERR_SPELL_UNLEARNED_S || You have unlearned %s.
|-
| 401 ||  ||  || ERR_PET_SPELL_ROOTED || Your pet is unable to move.
|-
| 402 ||  ||  || ERR_PET_SPELL_AFFECTING_COMBAT || Your pet is in combat.
|-
| 403 ||  ||  || ERR_PET_SPELL_OUT_OF_RANGE || Your pet is out of range.
|-
| 404 ||  ||  || ERR_PET_SPELL_NOT_BEHIND || Your pet must be behind its target.
|-
| 405 ||  ||  || ERR_PET_SPELL_TARGETS_DEAD || Your pet's target is dead.
|-
| 406 ||  ||  || ERR_PET_SPELL_DEAD || Your pet is dead.
|-
| 407 ||  ||  || ERR_PET_SPELL_NOPATH || No path available for your pet
|-
| 408 ||  ||  || ERR_ITEM_CANT_BE_DESTROYED || That item cannot be destroyed.
|-
| 409 ||  ||  || ERR_TICKET_ALREADY_EXISTS || You already have a GM ticket.
|-
| 410 ||  ||  || ERR_TICKET_CREATE_ERROR || Error creating GM ticket.
|-
| 411 ||  ||  || ERR_TICKET_UPDATE_ERROR || Error updating GM ticket.
|-
| 412 ||  ||  || ERR_TICKET_DB_ERROR || Error retrieving GM ticket.
|-
| 413 ||  ||  || ERR_TICKET_NO_TEXT || You must enter text for your ticket.
|-
| 414 ||  ||  || ERR_TICKET_TEXT_TOO_LONG || Your ticket text was too long.
|-
| 415 ||  ||  || ERR_OBJECT_IS_BUSY || That object is busy.
|-
| 416 ||  ||  || ERR_EXHAUSTION_WELLRESTED || You feel well rested.
|-
| 417 ||  ||  || ERR_EXHAUSTION_RESTED || You feel rested.
|-
| 418 ||  ||  || ERR_EXHAUSTION_NORMAL || You are no longer rested.
|-
| 419 ||  ||  || ERR_EXHAUSTION_TIRED || You feel tired.
|-
| 420 ||  ||  || ERR_EXHAUSTION_EXHAUSTED || You feel exhausted.
|-
| 421 ||  ||  || ERR_NO_ITEMS_WHILE_SHAPESHIFTED || Can't use items while shapeshifted.
|-
| 422 ||  ||  || ERR_CANT_INTERACT_SHAPESHIFTED || Can't speak while shapeshifted.
|-
| 423 ||  ||  || ERR_REALM_NOT_FOUND || Cannot find that realm.
|-
| 424 ||  || 59 || ERR_MAIL_QUEST_ITEM || You can't mail quest items.
|-
| 425 ||  || 59 || ERR_MAIL_BOUND_ITEM || You can't mail soulbound items.
|-
| 426 ||  ||  || ERR_MAIL_CONJURED_ITEM || You cannot mail conjured items
|-
| 427 ||  ||  || ERR_MAIL_BAG || You can't mail non-empty bags.
|-
| 428 ||  ||  || ERR_MAIL_TO_SELF || You can't send mail to yourself.
|-
| 429 ||  ||  || ERR_MAIL_TARGET_NOT_FOUND || Cannot find mail recipient.
|-
| 430 ||  ||  || ERR_MAIL_DATABASE_ERROR || Internal mail database error.
|-
| 431 ||  ||  || ERR_MAIL_DELETE_ITEM_ERROR || You can't delete that.
|-
| 432 ||  ||  || ERR_MAIL_WRAPPED_COD || You can't send wrapped items C.O.D.
|-
| 433 ||  ||  || ERR_MAIL_CANT_SEND_REALM || You can't send mail to that realm.
|-
| 434 ||  ||  || ERR_MAIL_TEMP_RETURN_OUTAGE || Mail return temporarily unavailable
|-
| 435 ||  ||  || ERR_MAIL_RECEPIENT_CANT_RECEIVE_MAIL || Recipient can't receive mail at this time.
|-
| 436 ||  ||  || ERR_MAIL_SENT || Mail sent.
|-
| 437 ||  ||  || ERR_NOT_HAPPY_ENOUGH || 
|-
| 438 ||  ||  || ERR_USE_CANT_IMMUNE || You can't do that while you are immune.
|-
| 439 ||  ||  || ERR_CANT_BE_DISENCHANTED || Item cannot be disenchanted
|-
| 440 ||  ||  || ERR_CANT_USE_DISARMED || You cannot use an item that is disarmed.
|-
| 441 ||  ||  || ERR_AUCTION_DATABASE_ERROR || Internal auction error.
|-
| 442 ||  ||  || ERR_AUCTION_HIGHER_BID || There is already a higher bid on that item.
|-
| 443 ||  ||  || ERR_AUCTION_ALREADY_BID || You have already bid on this item.
|-
| 444 ||  ||  || ERR_AUCTION_OUTBID_S || You have been outbid on %s.
|-
| 445 ||  ||  || ERR_AUCTION_WON_S || You won an auction for %s
|-
| 446 ||  ||  || ERR_AUCTION_REMOVED_S || Your auction of %s has been canceled by the seller.
|-
| 447 ||  ||  || ERR_AUCTION_BID_PLACED || Bid accepted.
|-
| 448 ||  ||  || ERR_LOGOUT_FAILED || You can't logout now.
|-
| 449 ||  ||  || ERR_QUEST_PUSH_SUCCESS_S || Sharing quest with %s...
|-
| 450 ||  ||  || ERR_QUEST_PUSH_INVALID_S || %s is not eligible for that quest.
|-
| 451 ||  ||  || ERR_QUEST_PUSH_INVALID_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are not eligible for that quest.
|-
| 452 ||  ||  || ERR_QUEST_PUSH_ACCEPTED_S || %s has accepted your quest.
|-
| 453 ||  ||  || ERR_QUEST_PUSH_DECLINED_S || %s has declined your quest.
|-
| 454 ||  ||  || ERR_QUEST_PUSH_BUSY_S || %s is busy.
|-
| 455 ||  ||  || ERR_QUEST_PUSH_DEAD_S || %s is dead.
|-
| 456 ||  ||  || ERR_QUEST_PUSH_DEAD_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are dead.
|-
| 457 ||  ||  || ERR_QUEST_PUSH_LOG_FULL_S || %s's quest log is full.
|-
| 458 ||  ||  || ERR_QUEST_PUSH_LOG_FULL_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. Your quest log is full.
|-
| 459 ||  ||  || ERR_QUEST_PUSH_ONQUEST_S || %s is already on that quest.
|-
| 460 ||  ||  || ERR_QUEST_PUSH_ONQUEST_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are already on that quest.
|-
| 461 ||  ||  || ERR_QUEST_PUSH_ALREADY_DONE_S || %s has completed that quest.
|-
| 462 ||  ||  || ERR_QUEST_PUSH_ALREADY_DONE_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You have completed that quest.
|-
| 463 ||  ||  || ERR_QUEST_PUSH_NOT_DAILY_S || That quest cannot be shared today.
|-
| 464 ||  ||  || ERR_QUEST_PUSH_TIMER_EXPIRED_S || Quest sharing timer has expired.
|-
| 465 ||  ||  || ERR_QUEST_PUSH_NOT_IN_PARTY_S || You are not in a party.
|-
| 466 ||  ||  || ERR_QUEST_PUSH_DIFFERENT_SERVER_DAILY_S || %s is not eligible for that quest today.
|-
| 467 ||  ||  || ERR_QUEST_PUSH_DIFFERENT_SERVER_DAILY_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are not eligible for that quest today.
|-
| 468 ||  ||  || ERR_QUEST_PUSH_NOT_ALLOWED_S || That quest cannot be shared.
|-
| 469 ||  ||  || ERR_QUEST_PUSH_PREREQUISITE_S || %s hasn't completed all of the prerequisite quests required for that quest.
|-
| 470 ||  ||  || ERR_QUEST_PUSH_PREREQUISITE_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You must complete all of the prerequisite quests first.
|-
| 471 ||  ||  || ERR_QUEST_PUSH_LOW_LEVEL_S || %s is too low level for that quest.
|-
| 472 ||  ||  || ERR_QUEST_PUSH_LOW_LEVEL_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are too low level for that quest.
|-
| 473 ||  ||  || ERR_QUEST_PUSH_HIGH_LEVEL_S || %s is too high level for that quest.
|-
| 474 ||  ||  || ERR_QUEST_PUSH_HIGH_LEVEL_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are too high level for that quest.
|-
| 475 ||  ||  || ERR_QUEST_PUSH_CLASS_S || %s is the wrong class for that quest.
|-
| 476 ||  ||  || ERR_QUEST_PUSH_CLASS_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are the wrong class for that quest.
|-
| 477 ||  ||  || ERR_QUEST_PUSH_RACE_S || %s is the wrong race for that quest.
|-
| 478 ||  ||  || ERR_QUEST_PUSH_RACE_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are the wrong race for that quest.
|-
| 479 ||  ||  || ERR_QUEST_PUSH_LOW_FACTION_S || %s's reputation is too low for that quest.
|-
| 480 ||  ||  || ERR_QUEST_PUSH_LOW_FACTION_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. Your reputation is too low for that quest.
|-
| 481 ||  ||  || ERR_QUEST_PUSH_EXPANSION_S || %s doesn't own the required expansion for that quest.
|-
| 482 ||  ||  || ERR_QUEST_PUSH_EXPANSION_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You do not own the required expansion for that quest.
|-
| 483 ||  ||  || ERR_QUEST_PUSH_NOT_GARRISON_OWNER_S || %s must own a garrison to accept that quest.
|-
| 484 ||  ||  || ERR_QUEST_PUSH_NOT_GARRISON_OWNER_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You must own a garrison to accept that quest.
|-
| 485 ||  ||  || ERR_QUEST_PUSH_WRONG_COVENANT_S || %s is in the wrong covenant for that quest.
|-
| 486 ||  ||  || ERR_QUEST_PUSH_WRONG_COVENANT_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are in the wrong covenant for that quest.
|-
| 487 ||  ||  || ERR_QUEST_PUSH_NEW_PLAYER_EXPERIENCE_S || %s must complete Exile's Reach to accept that quest.
|-
| 488 ||  ||  || ERR_QUEST_PUSH_NEW_PLAYER_EXPERIENCE_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You must complete Exile's Reach to accept that quest.
|-
| 489 ||  ||  || ERR_QUEST_PUSH_WRONG_FACTION_S || %s is the wrong faction for that quest.
|-
| 490 ||  ||  || ERR_QUEST_PUSH_WRONG_FACTION_TO_RECIPIENT_S || %s's attempt to share quest "%s" failed. You are the wrong faction for that quest.
|-
| 491 ||  ||  || ERR_QUEST_PUSH_CROSS_FACTION_RESTRICTED_S || Quests can't be shared in cross-faction groups.
|-
| 492 ||  ||  || ERR_RAID_GROUP_LOWLEVEL || You are too low level to enter this location.
|-
| 493 ||  ||  || ERR_RAID_GROUP_ONLY || You must be in a raid group to enter this location.
|-
| 494 ||  ||  || ERR_RAID_GROUP_FULL || The instance is full.
|-
| 495 ||  ||  || ERR_RAID_GROUP_REQUIREMENTS_UNMATCH || You do not meet the requirements to enter this location.
|-
| 496 ||  ||  || ERR_CORPSE_IS_NOT_IN_INSTANCE || Your corpse is not in that instance
|-
| 497 ||  ||  || ERR_PVP_KILL_HONORABLE || 
|-
| 498 ||  ||  || ERR_PVP_KILL_DISHONORABLE || 
|-
| 499 ||  ||  || ERR_SPELL_FAILED_ALREADY_AT_FULL_HEALTH || You are already at full Health
|-
| 500 ||  ||  || ERR_SPELL_FAILED_ALREADY_AT_FULL_MANA || You are already at full Mana
|-
| 501 ||  ||  || ERR_SPELL_FAILED_ALREADY_AT_FULL_POWER_S || You are already at full %s
|-
| 502 ||  ||  || ERR_AUTOLOOT_MONEY_S || You loot %s
|-
| 503 ||  ||  || ERR_GENERIC_STUNNED || You are stunned
|-
| 504 ||  ||  || ERR_GENERIC_THROTTLE || You're doing that too fast
|-
| 505 ||  ||  || ERR_CLUB_FINDER_SEARCHING_TOO_FAST || You are searching too fast, please wait a few moments before searching again.
|-
| 506 ||  ||  || ERR_TARGET_STUNNED || Target is stunned
|-
| 507 ||  ||  || ERR_MUST_REPAIR_DURABILITY || You must repair that item's durability to use it.
|-
| 508 ||  ||  || ERR_RAID_YOU_JOINED || You have joined a raid group. (While in a raid, you cannot earn credit towards most non-raid quests.)
|-
| 509 ||  ||  || ERR_RAID_YOU_LEFT || You have left the raid group.
|-
| 510 ||  ||  || ERR_INSTANCE_GROUP_JOINED_WITH_PARTY || You are in both a party and an instance group. You may communicate with your party with "/p" and with your instance group with "/i".
|-
| 511 ||  ||  || ERR_INSTANCE_GROUP_JOINED_WITH_RAID || You are in both a raid and an instance group. You may communicate with your raid with "/ra" and with your instance group with "/i".
|-
| 512 ||  ||  || ERR_RAID_MEMBER_ADDED_S || %s has joined the raid group.
|-
| 513 ||  ||  || ERR_RAID_MEMBER_REMOVED_S || %s has left the raid group.
|-
| 514 ||  ||  || ERR_INSTANCE_GROUP_ADDED_S || %s has joined the instance group.
|-
| 515 ||  ||  || ERR_INSTANCE_GROUP_REMOVED_S || %s has left the instance group.
|-
| 516 ||  ||  || ERR_CLICK_ON_ITEM_TO_FEED || Click on an item to feed to your pet
|-
| 517 ||  ||  || ERR_TOO_MANY_CHAT_CHANNELS || You can only be in %d channels at a time.
|-
| 518 ||  ||  || ERR_LOOT_ROLL_PENDING || That item is still being rolled for.
|-
| 519 ||  ||  || ERR_LOOT_PLAYER_NOT_FOUND || Player not found
|-
| 520 ||  ||  || ERR_NOT_IN_RAID || You are not in a raid group
|-
| 521 ||  ||  || ERR_LOGGING_OUT || You are logging out
|-
| 522 ||  ||  || ERR_TARGET_LOGGING_OUT || That player is logging out
|-
| 523 ||  ||  || ERR_NOT_WHILE_MOUNTED || You can't do that while mounted.
|-
| 524 ||  ||  || ERR_NOT_WHILE_SHAPESHIFTED || You can't do that while shapeshifted.
|-
| 525 ||  ||  || ERR_NOT_IN_COMBAT || You can't do that while in combat
|-
| 526 ||  ||  || ERR_NOT_WHILE_DISARMED || You can't do that while disarmed
|-
| 527 ||  ||  || ERR_PET_BROKEN || Your pet has run away
|-
| 528 ||  ||  || ERR_TALENT_WIPE_ERROR || You have not chosen any talents.
|-
| 529 ||  ||  || ERR_SPEC_WIPE_ERROR || You have not chosen a class specialization.
|-
| 530 ||  ||  || ERR_GLYPH_WIPE_ERROR || You have not chosen any glyphs.
|-
| 531 ||  ||  || ERR_PET_SPEC_WIPE_ERROR || You have not chosen a specialization for your pet.
|-
| 532 ||  ||  || ERR_FEIGN_DEATH_RESISTED || Resisted
|-
| 533 || 8458 ||  || ERR_MEETING_STONE_IN_QUEUE_S || You are now in the queue to join a party for %s.
|-
| 534 ||  ||  || ERR_MEETING_STONE_LEFT_QUEUE_S || You have left the queue to join a party for %s.
|-
| 535 ||  ||  || ERR_MEETING_STONE_OTHER_MEMBER_LEFT || Party member has left.  Looking for a new party in the meeting stone queue.
|-
| 536 ||  ||  || ERR_MEETING_STONE_PARTY_KICKED_FROM_QUEUE || 
|-
| 537 ||  ||  || ERR_MEETING_STONE_MEMBER_STILL_IN_QUEUE || Looking for a new party in the meeting stone queue.
|-
| 538 ||  ||  || ERR_MEETING_STONE_SUCCESS || Your group is complete, you have left the meeting stone queue.
|-
| 539 ||  ||  || ERR_MEETING_STONE_IN_PROGRESS || You are still seeking more members through the meeting stone.
|-
| 540 ||  ||  || ERR_MEETING_STONE_MEMBER_ADDED_S || %s has been added to the group by the meeting stone.
|-
| 541 ||  ||  || ERR_MEETING_STONE_GROUP_FULL || You are already in a full group
|-
| 542 ||  ||  || ERR_MEETING_STONE_NOT_LEADER || Only the party leader can leave the meeting stone queue
|-
| 543 ||  ||  || ERR_MEETING_STONE_INVALID_LEVEL || You do not meet the level requirements of this meeting stone.
|-
| 544 ||  ||  || ERR_MEETING_STONE_TARGET_NOT_IN_PARTY || Your target is not in the party
|-
| 545 ||  ||  || ERR_MEETING_STONE_TARGET_INVALID_LEVEL || Your target does not meet the level requirements of this meeting stone.
|-
| 546 ||  ||  || ERR_MEETING_STONE_MUST_BE_LEADER || You must be the party leader to interact with the meeting stone
|-
| 547 ||  ||  || ERR_MEETING_STONE_NO_RAID_GROUP || You cannot use a meeting stone while in a raid group
|-
| 548 ||  ||  || ERR_MEETING_STONE_NEED_PARTY || You need to be in a party to use a meeting stone
|-
| 549 ||  ||  || ERR_MEETING_STONE_NOT_FOUND || Player not found.
|-
| 550 ||  ||  || ERR_MEETING_STONE_TARGET_IN_VEHICLE || Your target is in a vehicle
|-
| 551 ||  ||  || ERR_GUILDEMBLEM_SAME || Not saved, your tabard is already like that.
|-
| 552 ||  ||  || ERR_EQUIP_TRADE_ITEM || That item is currently being traded
|-
| 553 ||  ||  || ERR_PVP_TOGGLE_ON || PvP combat toggled on
|-
| 554 ||  ||  || ERR_PVP_TOGGLE_OFF || PvP combat toggled off
|-
| 555 ||  ||  || ERR_GROUP_JOIN_BATTLEGROUND_DESERTERS || You cannot join the battleground yet because you or one of your party members is flagged as a Deserter.
|-
| 556 ||  ||  || ERR_GROUP_JOIN_BATTLEGROUND_DEAD || You cannot join the battleground because you or one of your party members is dead.
|-
| 557 ||  ||  || ERR_GROUP_JOIN_BATTLEGROUND_S || Your group has joined the queue for %s.
|-
| 558 ||  ||  || ERR_GROUP_JOIN_BATTLEGROUND_FAIL || Your group has joined a battleground queue, but you are not eligible.
|-
| 559 ||  ||  || ERR_GROUP_JOIN_BATTLEGROUND_TOO_MANY || Your group is too big to join that battleground
|-
| 560 ||  ||  || ERR_SOLO_JOIN_BATTLEGROUND_S || You have joined the queue for %s.
|-
| 561 ||  ||  || ERR_JOIN_SINGLE_SCENARIO_S || You have joined the queue for %s.
|-
| 562 ||  ||  || ERR_BATTLEGROUND_TOO_MANY_QUEUES || You can only be queued for 2 battles at once
|-
| 563 ||  ||  || ERR_BATTLEGROUND_CANNOT_QUEUE_FOR_RATED || You cannot queue for a rated match while queued for other battles
|-
| 564 ||  ||  || ERR_BATTLEDGROUND_QUEUED_FOR_RATED || You cannot queue for another battle while queued for a rated match
|-
| 565 ||  ||  || ERR_BATTLEGROUND_TEAM_LEFT_QUEUE || Your team has left the queue
|-
| 566 ||  ||  || ERR_BATTLEGROUND_NOT_IN_BATTLEGROUND || You can't do that in a battleground.
|-
| 567 ||  ||  || ERR_ALREADY_IN_ARENA_TEAM_S || %s is already in an arena team of that size.
|-
| 568 ||  ||  || ERR_INVALID_PROMOTION_CODE || Couldn't validate code, please try again.
|-
| 569 ||  ||  || ERR_BG_PLAYER_JOINED_SS || [%s] has joined the battle.
|-
| 570 ||  ||  || ERR_BG_PLAYER_LEFT_S || %s has left the battle
|-
| 571 ||  ||  || ERR_RESTRICTED_ACCOUNT || Free Trial accounts cannot perform that action
|-
| 572 ||  ||  || ERR_RESTRICTED_ACCOUNT_TRIAL || Free Trial accounts cannot perform that action
|-
| 573 ||  ||  || ERR_PLAY_TIME_EXCEEDED || Maximum play time exceeded
|-
| 574 ||  ||  || ERR_APPROACHING_PARTIAL_PLAY_TIME || You have %s until you enter tired time.  Your rewards will be cut in half.
|-
| 575 ||  ||  || ERR_APPROACHING_PARTIAL_PLAY_TIME_2 || Your accumulated online time is %s hours.
|-
| 576 ||  ||  || ERR_APPROACHING_NO_PLAY_TIME || You have %s until you enter unhealthy time, at which point you will no longer receive experience or loot until you have logged out for 5 hours.
|-
| 577 ||  ||  || ERR_APPROACHING_NO_PLAY_TIME_2 || You are in tired time, and your benefits have been reduced to 50%% of normal. For the sake of your own health, please go offline and rest, do some exercise, and arrange your time properly.
|-
| 578 ||  ||  || ERR_UNHEALTHY_TIME || You are in unhealthy time, you should log off now.
|-
| 579 ||  ||  || ERR_CHAT_RESTRICTED_TRIAL || Free Trial accounts cannot send unlimited tells. You must wait before you can send tells to more players.  [Click To Upgrade]
|-
| 580 ||  ||  || ERR_CHAT_THROTTLED || The number of messages that can be sent is limited, please wait to send another message.
|-
| 581 ||  ||  || ERR_MAIL_REACHED_CAP || You have reached the in-game cap of unique mail recipients
|-
| 582 ||  ||  || ERR_INVALID_RAID_TARGET || You cannot target mark enemy players
|-
| 583 ||  ||  || ERR_RAID_LEADER_READY_CHECK_START_S || %s has initiated a ready check.
|-
| 584 ||  ||  || ERR_READY_CHECK_IN_PROGRESS || You are already running a ready check
|-
| 585 ||  ||  || ERR_READY_CHECK_THROTTLED || You can't do that yet
|-
| 586 ||  ||  || ERR_DUNGEON_DIFFICULTY_FAILED || Unable to change Dungeon Difficulty
|-
| 587 ||  ||  || ERR_DUNGEON_DIFFICULTY_CHANGED_S || Dungeon Difficulty set to %s.
|-
| 588 ||  ||  || ERR_TRADE_WRONG_REALM || You may only trade conjured items to players from other realms
|-
| 589 ||  ||  || ERR_TRADE_NOT_ON_TAPLIST || You may only trade bound items to players that were originally eligible to loot the item
|-
| 590 ||  ||  || ERR_CHAT_PLAYER_AMBIGUOUS_S || %s: More than one player matches, type more of their server name
|-
| 591 ||  ||  || ERR_LOOT_CANT_LOOT_THAT_NOW || You can't loot that item now.
|-
| 592 ||  ||  || ERR_LOOT_MASTER_INV_FULL || That player's inventory is full
|-
| 593 ||  ||  || ERR_LOOT_MASTER_UNIQUE_ITEM || Player has too many of that item already
|-
| 594 ||  ||  || ERR_LOOT_MASTER_OTHER || Can't assign item to that player
|-
| 595 ||  ||  || ERR_FILTERING_YOU_S || Unable to send chat to %s because your message contained reserved words.
|-
| 596 ||  ||  || ERR_USE_PREVENTED_BY_MECHANIC_S || Can't use while %s.
|-
| 597 ||  ||  || ERR_ITEM_UNIQUE_EQUIPPABLE || You cannot equip more than one of those.
|-
| 598 ||  ||  || ERR_LFG_LEADER_IS_LFM_S || You can't do that while %s is looking for more members.
|-
| 599 ||  ||  || ERR_LFG_PENDING || You cannot invite other players while in a random group.
|-
| 600 ||  ||  || ERR_CANT_SPEAK_LANGAGE || You cannot speak that language.
|-
| 601 ||  ||  || ERR_VENDOR_MISSING_TURNINS || You do not have the required items for that purchase
|-
| 602 ||  ||  || ERR_BATTLEGROUND_NOT_IN_TEAM || Your group is not in the same team
|-
| 603 ||  ||  || ERR_NOT_IN_BATTLEGROUND || You are not in a battleground
|-
| 604 ||  ||  || ERR_NOT_ENOUGH_HONOR_POINTS || You don't have enough honor
|-
| 605 ||  ||  || ERR_NOT_ENOUGH_ARENA_POINTS || You don't have enough arena points
|-
| 606 ||  ||  || ERR_SOCKETING_REQUIRES_META_GEM || That slot requires a meta gem
|-
| 607 ||  ||  || ERR_SOCKETING_META_GEM_ONLY_IN_METASLOT || Meta gems can only be placed in meta gem slots
|-
| 608 ||  ||  || ERR_SOCKETING_REQUIRES_HYDRAULIC_GEM || That slot requires a Crystal of Fear.
|-
| 609 ||  ||  || ERR_SOCKETING_HYDRAULIC_GEM_ONLY_IN_HYDRAULICSLOT || Crystals of Fear can only be placed in Sha-Touched weapons.
|-
| 610 ||  ||  || ERR_SOCKETING_REQUIRES_COGWHEEL_GEM || That slot requires a Cogwheel
|-
| 611 ||  ||  || ERR_SOCKETING_COGWHEEL_GEM_ONLY_IN_COGWHEELSLOT || Cogwheels can only be placed in Cogwheel slots
|-
| 612 ||  ||  || ERR_SOCKETING_ITEM_TOO_LOW_LEVEL || The item is too low level to accept that gem
|-
| 613 ||  ||  || ERR_ITEM_MAX_COUNT_SOCKETED || You have the maximum number of those gems in your inventory or socketed into items.
|-
| 614 ||  ||  || ERR_SYSTEM_DISABLED || This system is currently disabled.
|-
| 615 || 847 ||  || ERR_QUEST_FAILED_TOO_MANY_DAILY_QUESTS_I || You have already completed %d daily quests today
|-
| 616 ||  ||  || ERR_ITEM_MAX_COUNT_EQUIPPED_SOCKETED || You have the maximum number of those gems socketed into equipped items.
|-
| 617 ||  ||  || ERR_ITEM_UNIQUE_EQUIPPABLE_SOCKETED || You cannot socket more than one of those gems into a single item.
|-
| 618 ||  ||  || ERR_USER_SQUELCHED || We have temporarily suspended your chat and mail privileges. Check your email for more details.
|-
| 619 ||  ||  || ERR_ACCOUNT_SILENCED || Can't do that while your account is silenced
|-
| 620 ||  ||  || ERR_PARTY_MEMBER_SILENCED || Can't do that when someone in your group is silenced.
|-
| 621 ||  ||  || ERR_PARTY_MEMBER_SILENCED_LFG_DELIST || Your group has been delisted because someone in your group is silenced.
|-
| 622 ||  ||  || ERR_TOO_MUCH_GOLD || At gold limit
|-
| 623 ||  ||  || ERR_NOT_BARBER_SITTING || You must be sitting in a barber chair
|-
| 624 || 847 ||  || ERR_QUEST_FAILED_CAIS || You cannot complete quests once you have reached tired time
|-
| 625 ||  ||  || ERR_INVITE_RESTRICTED_TRIAL || Free Trial accounts cannot invite characters into groups. [Click To Upgrade]
|-
| 626 ||  ||  || ERR_VOICE_IGNORE_FULL || You can't voice mute any more players.
|-
| 627 ||  ||  || ERR_VOICE_IGNORE_SELF || You can't voice mute yourself.
|-
| 628 ||  ||  || ERR_VOICE_IGNORE_NOT_FOUND || Player not found.
|-
| 629 ||  ||  || ERR_VOICE_IGNORE_ALREADY_S || %s is already being voice muted.
|-
| 630 ||  ||  || ERR_VOICE_IGNORE_ADDED_S || %s is now being voice muted.
|-
| 631 ||  ||  || ERR_VOICE_IGNORE_REMOVED_S || %s is no longer being voice muted.
|-
| 632 ||  ||  || ERR_VOICE_IGNORE_AMBIGUOUS || That name is ambiguous, type more of the player's server name.
|-
| 633 ||  ||  || ERR_VOICE_IGNORE_DELETED || Voice mute removed because the character no longer exists.
|-
| 634 ||  ||  || ERR_UNKNOWN_MACRO_OPTION_S || Unknown macro option: %s
|-
| 635 ||  ||  || ERR_NOT_DURING_ARENA_MATCH || You can't do that while in an arena match
|-
| 636 ||  ||  || ERR_NOT_IN_RATED_BATTLEGROUND || You can't do that in a rated battleground.
|-
| 637 ||  ||  || ERR_PLAYER_SILENCED || A group leader has removed your voice privileges.
|-
| 638 ||  ||  || ERR_PLAYER_UNSILENCED || A group leader has restored your voice privileges.
|-
| 639 ||  ||  || ERR_COMSAT_DISCONNECT || Connection lost to Voice Chat service.
|-
| 640 ||  ||  || ERR_COMSAT_RECONNECT_ATTEMPT || Voice Chat service restored!
|-
| 641 ||  ||  || ERR_COMSAT_CONNECT_FAIL || Cannot connect to voice chat service.
|-
| 642 ||  ||  || ERR_MAIL_INVALID_ATTACHMENT_SLOT || You cannot attach more than 12 items to mail.
|-
| 643 ||  ||  || ERR_MAIL_TOO_MANY_ATTACHMENTS || A mail included too many attachments.
|-
| 644 ||  ||  || ERR_MAIL_INVALID_ATTACHMENT || A mail attachment was invalid.
|-
| 645 ||  ||  || ERR_MAIL_ATTACHMENT_EXPIRED || That item has expired.
|-
| 646 ||  ||  || ERR_VOICE_CHAT_PARENTAL_DISABLE_MIC || Microphone has been disabled by Parental Controls.
|-
| 647 ||  ||  || ERR_PROFANE_CHAT_NAME || You may not create custom channels with profane names.
|-
| 648 ||  ||  || ERR_PLAYER_SILENCED_ECHO || You have removed the voice privileges of %s.
|-
| 649 ||  ||  || ERR_PLAYER_UNSILENCED_ECHO || You have restored the voice privileges of %s.
|-
| 650 ||  ||  || ERR_LOOT_CANT_LOOT_THAT || You don't meet the requirements to loot that item
|-
| 651 ||  ||  || ERR_ARENA_EXPIRED_CAIS || You may not queue while one or more of your team members is under the effect of restricted play.
|-
| 652 ||  ||  || ERR_GROUP_ACTION_THROTTLED || You have attempted too many group actions in a short period of time.  Please wait momentarily before attempting further group actions.
|-
| 653 ||  ||  || ERR_ALREADY_PICKPOCKETED || Your target has already had its pockets picked
|-
| 654 ||  ||  || ERR_NAME_INVALID || That name contains invalid characters.  Enter a new name.
|-
| 655 ||  ||  || ERR_NAME_NO_NAME || Please enter a name.
|-
| 656 ||  ||  || ERR_NAME_TOO_SHORT || That name is too short. Enter a new name.
|-
| 657 ||  ||  || ERR_NAME_TOO_LONG || That name is too long. Enter a new name.
|-
| 658 ||  ||  || ERR_NAME_MIXED_LANGUAGES || Names must use one language.  Enter a new name.
|-
| 659 ||  ||  || ERR_NAME_PROFANE || That name contains mature language.  Enter a new name.
|-
| 660 ||  ||  || ERR_NAME_RESERVED || That name is reserved.  Enter a new name.
|-
| 661 ||  ||  || ERR_NAME_THREE_CONSECUTIVE || You cannot use the same letter three times consecutively.  Enter a new name.
|-
| 662 ||  ||  || ERR_NAME_INVALID_SPACE || Names cannot start or end with a space.  Enter a new name.
|-
| 663 ||  ||  || ERR_NAME_CONSECUTIVE_SPACES || Consecutive spaces are not allowed.  Enter a new name.
|-
| 664 ||  ||  || ERR_NAME_RUSSIAN_CONSECUTIVE_SILENT_CHARACTERS || Consecutive silent characters are not allowed. Create a new name.
|-
| 665 ||  ||  || ERR_NAME_RUSSIAN_SILENT_CHARACTER_AT_BEGINNING_OR_END || Silent characters are now allowed at the beginning or end of a name. Create a new name.
|-
| 666 ||  ||  || ERR_NAME_DECLENSION_DOESNT_MATCH_BASE_NAME || Your declensions must match your original name.  Enter a new name.
|-
| 667 ||  ||  || ERR_RECRUIT_A_FRIEND_NOT_LINKED || You can only summon players who are linked to you through Recruit A Friend
|-
| 668 ||  ||  || ERR_RECRUIT_A_FRIEND_NOT_NOW || You cannot summon that player right now
|-
| 669 ||  ||  || ERR_RECRUIT_A_FRIEND_SUMMON_LEVEL_MAX || You cannot summon players above level %d
|-
| 670 ||  ||  || ERR_RECRUIT_A_FRIEND_SUMMON_COOLDOWN || You can only summon your friend once every thirty minutes
|-
| 671 ||  ||  || ERR_RECRUIT_A_FRIEND_SUMMON_OFFLINE || %s is offline and cannot be summoned
|-
| 672 ||  ||  || ERR_RECRUIT_A_FRIEND_INSUF_EXPAN_LVL || That player does not have the required expansion to access this area
|-
| 673 ||  ||  || ERR_RECRUIT_A_FRIEND_MAP_INCOMING_TRANSFER_NOT_ALLOWED || You cannot summon your friend here
|-
| 674 ||  || 59 || ERR_NOT_SAME_ACCOUNT || Account-bound items can only be given to your own characters.
|-
| 675 ||  ||  || ERR_BAD_ON_USE_ENCHANT || That item already has an activated ability
|-
| 676 ||  ||  || ERR_TRADE_SELF || You can't trade with yourself.
|-
| 677 ||  ||  || ERR_TOO_MANY_SOCKETS || That item has too many sockets
|-
| 678 ||  ||  || ERR_ITEM_MAX_LIMIT_CATEGORY_COUNT_EXCEEDED_IS || You can only carry %d %s.
|-
| 679 ||  ||  || ERR_TRADE_TARGET_MAX_LIMIT_CATEGORY_COUNT_EXCEEDED_IS || Your trade partner can only carry %d %s
|-
| 680 ||  ||  || ERR_ITEM_MAX_LIMIT_CATEGORY_SOCKETED_EXCEEDED_IS || You can only equip %d |4item:items; in the %s category
|-
| 681 ||  ||  || ERR_ITEM_MAX_LIMIT_CATEGORY_EQUIPPED_EXCEEDED_IS || You can only equip %d |4item:items; in the %s category
|-
| 682 ||  ||  || ERR_SHAPESHIFT_FORM_CANNOT_EQUIP || Cannot equip item in this form
|-
| 683 ||  ||  || ERR_ITEM_INVENTORY_FULL_SATCHEL || Your inventory is full. Your item has been delivered to your mailbox.
|-
| 684 ||  ||  || ERR_SCALING_STAT_ITEM_LEVEL_EXCEEDED || Your level is too high to use that item
|-
| 685 ||  ||  || ERR_SCALING_STAT_ITEM_LEVEL_TOO_LOW || Your level is too low to use that item
|-
| 686 ||  ||  || ERR_PURCHASE_LEVEL_TOO_LOW || You must reach level %d to purchase that item.
|-
| 687 ||  ||  || ERR_GROUP_SWAP_FAILED || Players in raid combat cannot change raid subgroups
|-
| 688 ||  ||  || ERR_INVITE_IN_COMBAT || You cannot invite a player in raid combat
|-
| 689 ||  ||  || ERR_INVALID_GLYPH_SLOT || That is not a valid glyph slot.
|-
| 690 ||  || 45 || ERR_GENERIC_NO_VALID_TARGETS || No valid targets.
|-
| 691 ||  ||  || ERR_CALENDAR_EVENT_ALERT_S || 
|-
| 692 ||  ||  || ERR_PET_LEARN_SPELL_S || Your pet has learned a new spell: %s.
|-
| 693 ||  ||  || ERR_PET_LEARN_ABILITY_S || Your pet has learned a new ability: %s.
|-
| 694 ||  ||  || ERR_PET_SPELL_UNLEARNED_S || Your pet has unlearned %s.
|-
| 695 ||  ||  || ERR_INVITE_UNKNOWN_REALM || You cannot invite players from that realm
|-
| 696 ||  ||  || ERR_INVITE_NO_PARTY_SERVER || Could not create a party
|-
| 697 ||  ||  || ERR_INVITE_PARTY_BUSY || Cannot invite additional players until the party is formed
|-
| 698 ||  ||  || ERR_PARTY_TARGET_AMBIGUOUS || There were multiple players in the party with that name, please include realm name
|-
| 699 ||  ||  || ERR_PARTY_LFG_INVITE_RAID_LOCKED || %s is locked to another instance.
|-
| 700 ||  ||  || ERR_PARTY_LFG_BOOT_LIMIT || You can not initiate any more party kicks.
|-
| 701 ||  ||  || ERR_PARTY_LFG_BOOT_COOLDOWN_S || You must wait %s before initiating another player kick.
|-
| 702 ||  ||  || ERR_PARTY_LFG_BOOT_NOT_ELIGIBLE_S || That player can not be kicked for another %s.
|-
| 703 ||  ||  || ERR_PARTY_LFG_BOOT_INPATIENT_TIMER_S || You may not initiate a vote to kick for another %s.
|-
| 704 ||  ||  || ERR_PARTY_LFG_BOOT_IN_PROGRESS || Another kick vote is already in progress.
|-
| 705 ||  ||  || ERR_PARTY_LFG_BOOT_TOO_FEW_PLAYERS || There are not enough players in the group to initate a vote.
|-
| 706 ||  ||  || ERR_PARTY_LFG_BOOT_VOTE_SUCCEEDED || The vote to kick %s has passed.
|-
| 707 ||  ||  || ERR_PARTY_LFG_BOOT_VOTE_FAILED || The vote to kick %s has failed.
|-
| 708 ||  ||  || ERR_PARTY_LFG_BOOT_IN_COMBAT || Players cannot be kicked while in combat, or shortly after combat.
|-
| 709 ||  ||  || ERR_PARTY_LFG_BOOT_DUNGEON_COMPLETE || Players cannot be kicked after the instance is complete.
|-
| 710 ||  ||  || ERR_PARTY_LFG_BOOT_LOOT_ROLLS || Players cannot be kicked during loot rolls.
|-
| 711 ||  ||  || ERR_PARTY_LFG_BOOT_VOTE_REGISTERED || Your request to kick %s has been successfully received. %d |4more request is:more requests are; needed to initiate a vote.
|-
| 712 ||  ||  || ERR_PARTY_PRIVATE_GROUP_ONLY || You cannot invite players to this group.
|-
| 713 ||  ||  || ERR_PARTY_LFG_TELEPORT_IN_COMBAT || You cannot teleport out of the dungeon while in combat.
|-
| 714 ||  ||  || ERR_RAID_DISALLOWED_BY_LEVEL || Character too low level for raid.
|-
| 715 ||  ||  || ERR_RAID_DISALLOWED_BY_CROSS_REALM || Cannot convert to raid while players from other realms are in the party.
|-
| 716 ||  ||  || ERR_PARTY_ROLE_NOT_AVAILABLE || Problem trying to fill your group's available roles
|-
| 717 ||  ||  || ERR_JOIN_LFG_OBJECT_FAILED || You failed to join the instance in progress
|-
| 718 ||  ||  || ERR_LFG_REMOVED_LEVELUP || You have been removed from the queue because you or someone in your group has gained a level.
|-
| 719 ||  ||  || ERR_LFG_REMOVED_XP_TOGGLE || You have been removed from the queue because you or someone in your group has toggled experience gain.
|-
| 720 ||  ||  || ERR_LFG_REMOVED_FACTION_CHANGE || You have been removed from the queue because you or someone in your group has selected a faction.
|-
| 721 ||  ||  || ERR_BATTLEGROUND_INFO_THROTTLED || You can't do that yet
|-
| 722 ||  ||  || ERR_BATTLEGROUND_ALREADY_IN || You are already in that battleground.
|-
| 723 ||  ||  || ERR_ARENA_TEAM_CHANGE_FAILED_QUEUED || Can't modify arena team while queued or in a match.
|-
| 724 ||  ||  || ERR_ARENA_TEAM_PERMISSIONS || You don't have permission to do that.
|-
| 725 ||  ||  || ERR_NOT_WHILE_FALLING || You can't do that while jumping or falling
|-
| 726 ||  ||  || ERR_NOT_WHILE_MOVING || Can't do that while moving.
|-
| 727 ||  ||  || ERR_NOT_WHILE_FATIGUED || You can't do that while fatigued
|-
| 728 ||  ||  || ERR_MAX_SOCKETS || That item cannot receive additional sockets
|-
| 729 ||  ||  || ERR_MULTI_CAST_ACTION_TOTEM_S || Only %s spells can go in that slot.
|-
| 730 ||  ||  || ERR_BATTLEGROUND_JOIN_LEVELUP || You have been removed from a PvP queue because you have gained a level.
|-
| 731 ||  ||  || ERR_REMOVE_FROM_PVP_QUEUE_XP_GAIN || You have been removed from a PVP queue because you have changed your XP gain settings
|-
| 732 ||  ||  || ERR_BATTLEGROUND_JOIN_XP_GAIN || Cannot join as a group unless all the members of your party have the same XP gain setting.
|-
| 733 ||  ||  || ERR_BATTLEGROUND_JOIN_MERCENARY || Cannot join as a group unless all the members of your party are flagged as a mercenary.
|-
| 734 ||  ||  || ERR_BATTLEGROUND_JOIN_TOO_MANY_HEALERS || You can not enter this bracket of arena with more than one healer.
|-
| 735 ||  ||  || ERR_BATTLEGROUND_JOIN_RATED_TOO_MANY_HEALERS || You can not enter a rated battleground with more than three healers.
|-
| 736 ||  ||  || ERR_BATTLEGROUND_JOIN_TOO_MANY_TANKS || You can not enter this bracket of arena with more than one tank.
|-
| 737 ||  ||  || ERR_BATTLEGROUND_JOIN_TOO_MANY_DAMAGE || You can not enter this bracket of arena with more than two damage dealers.
|-
| 738 ||  ||  || ERR_RAID_DIFFICULTY_FAILED || Unable to change Raid Difficulty
|-
| 739 ||  ||  || ERR_RAID_DIFFICULTY_CHANGED_S || Raid Difficulty set to %s.
|-
| 740 ||  ||  || ERR_LEGACY_RAID_DIFFICULTY_CHANGED_S || Legacy Raid Difficulty set to %s.
|-
| 741 ||  ||  || ERR_RAID_LOCKOUT_CHANGED_S || Raid Lockout set to %s.
|-
| 742 ||  ||  || ERR_RAID_CONVERTED_TO_PARTY || Raid converted to Party
|-
| 743 ||  ||  || ERR_PARTY_CONVERTED_TO_RAID || Party converted to Raid
|-
| 744 ||  ||  || ERR_PLAYER_DIFFICULTY_CHANGED_S || Difficulty set to %s.
|-
| 745 ||  ||  || ERR_GMRESPONSE_DB_ERROR || Error retrieving GM response.
|-
| 746 ||  ||  || ERR_BATTLEGROUND_JOIN_RANGE_INDEX || Cannot join the queue unless all members of your party are in the same level range.
|-
| 747 ||  ||  || ERR_ARENA_JOIN_RANGE_INDEX || Cannot join the queue unless all members of your party are in the same Arena level range.
|-
| 748 ||  ||  || ERR_REMOVE_FROM_PVP_QUEUE_FACTION_CHANGE || 
|-
| 749 ||  ||  || ERR_BATTLEGROUND_JOIN_FAILED || Join as a group failed
|-
| 750 ||  ||  || ERR_BATTLEGROUND_JOIN_NO_VALID_SPEC_FOR_ROLE || Role check failed because one of your party members selected an invalid role.
|-
| 751 ||  ||  || ERR_BATTLEGROUND_JOIN_RESPEC || You have been removed from a PvP queue because your specialization changed.
|-
| 752 ||  ||  || ERR_BATTLEGROUND_INVITATION_DECLINED || Your War Game invitation has been declined
|-
| 753 ||  ||  || ERR_BATTLEGROUND_JOIN_TIMED_OUT || %s was unavailable to join the queue.
|-
| 754 ||  ||  || ERR_BATTLEGROUND_DUPE_QUEUE || Someone in your group is already queued for that.
|-
| 755 ||  ||  || ERR_BATTLEGROUND_JOIN_MUST_COMPLETE_QUEST || You have been removed from a PvP queue because someone is missing required quest completion.
|-
| 756 ||  ||  || ERR_IN_BATTLEGROUND_RESPEC || This specialization doesn't match your assigned role.
|-
| 757 ||  ||  || ERR_MAIL_LIMITED_DURATION_ITEM || You cannot mail items with a limited duration
|-
| 758 ||  ||  || ERR_YELL_RESTRICTED_TRIAL || Free Trial accounts cannot yell. [Click To Upgrade]
|-
| 759 ||  ||  || ERR_CHAT_RAID_RESTRICTED_TRIAL || Free Trial accounts cannot send messages to raid channel.  [Click To Upgrade]
|-
| 760 ||  ||  || ERR_LFG_ROLE_CHECK_FAILED || The Role Check has failed.
|-
| 761 ||  ||  || ERR_LFG_ROLE_CHECK_FAILED_TIMEOUT || Role Check failed because a group member did not respond.
|-
| 762 ||  ||  || ERR_LFG_ROLE_CHECK_FAILED_NOT_VIABLE || Role Check failed because your group is not viable.
|-
| 763 ||  ||  || ERR_LFG_READY_CHECK_FAILED || The Ready Check has failed.
|-
| 764 ||  ||  || ERR_LFG_READY_CHECK_FAILED_TIMEOUT || Ready Check failed because a group member did not respond.
|-
| 765 ||  ||  || ERR_LFG_GROUP_FULL || Your group is already full.
|-
| 766 ||  ||  || ERR_LFG_NO_LFG_OBJECT || Internal LFG Error.
|-
| 767 ||  ||  || ERR_LFG_NO_SLOTS_PLAYER || You do not meet the requirements for the chosen dungeons.
|-
| 768 ||  ||  || ERR_LFG_NO_SLOTS_PARTY || The following players do not meet the requirements for the chosen dungeons: %s
|-
| 769 ||  ||  || ERR_LFG_NO_SPEC || You must choose a class specialization before starting this event
|-
| 770 ||  ||  || ERR_LFG_MISMATCHED_SLOTS || You cannot mix dungeons, raids, and random when picking dungeons.
|-
| 771 ||  ||  || ERR_LFG_MISMATCHED_SLOTS_LOCAL_XREALM || You cannot mix realm-only and x-realm entries when listing your name in other raids.
|-
| 772 ||  ||  || ERR_LFG_PARTY_PLAYERS_FROM_DIFFERENT_REALMS || The dungeon you chose does not support players from multiple realms.
|-
| 773 ||  ||  || ERR_LFG_MEMBERS_NOT_PRESENT || One or more group members are pending invites or disconnected.
|-
| 774 ||  ||  || ERR_LFG_GET_INFO_TIMEOUT || Could not retrieve information about some party members.
|-
| 775 ||  ||  || ERR_LFG_INVALID_SLOT || One or more dungeons was not valid.
|-
| 776 ||  ||  || ERR_LFG_DESERTER_PLAYER || You can not queue for dungeons until your deserter debuff wears off.
|-
| 777 ||  ||  || ERR_LFG_DESERTER_PARTY || One or more party members has a deserter debuff.
|-
| 778 ||  ||  || ERR_LFG_DEAD || You cannot queue because you or one of your party members is dead.
|-
| 779 ||  ||  || ERR_LFG_RANDOM_COOLDOWN_PLAYER || You can not queue for random dungeons while on random dungeon cooldown.
|-
| 780 ||  ||  || ERR_LFG_RANDOM_COOLDOWN_PARTY || One or more party members are on random dungeon cooldown.
|-
| 781 ||  ||  || ERR_LFG_TOO_MANY_MEMBERS || You have too many group members to queue for that.
|-
| 782 ||  ||  || ERR_LFG_TOO_FEW_MEMBERS || You do not have enough group members to queue for that.
|-
| 783 ||  ||  || ERR_LFG_PROPOSAL_FAILED || Someone has declined the invite. You have been returned to the front of the queue.
|-
| 784 ||  ||  || ERR_LFG_PROPOSAL_DECLINED_SELF || You have been removed from the queue because you did not accept the invitation.
|-
| 785 ||  ||  || ERR_LFG_PROPOSAL_DECLINED_PARTY || You have been removed from the queue because someone in your party did not accept the invitation.
|-
| 786 ||  ||  || ERR_LFG_NO_SLOTS_SELECTED || You did not select any valid slots.
|-
| 787 ||  ||  || ERR_LFG_NO_ROLES_SELECTED || You must select at least one role.
|-
| 788 ||  ||  || ERR_LFG_ROLE_CHECK_INITIATED || A role check has been initiated. Your group will be queued when all members have selected a role.
|-
| 789 ||  ||  || ERR_LFG_READY_CHECK_INITIATED || A ready check has been initiated. Your group will be queued when all members have indicated they are ready.
|-
| 790 ||  ||  || ERR_LFG_PLAYER_DECLINED_ROLE_CHECK || %s has not selected any roles.
|-
| 791 ||  ||  || ERR_LFG_PLAYER_DECLINED_READY_CHECK || %s is not ready.
|-
| 792 ||  ||  || ERR_LFG_JOINED_QUEUE || You are now queued in the Dungeon Finder.
|-
| 793 ||  ||  || ERR_LFG_JOINED_FLEX_QUEUE || You are now queued for Flexible Raids.
|-
| 794 ||  ||  || ERR_LFG_JOINED_RF_QUEUE || You are now queued in the Raid Finder.
|-
| 795 ||  ||  || ERR_LFG_JOINED_SCENARIO_QUEUE || You are now queued for Scenarios.
|-
| 796 ||  ||  || ERR_LFG_JOINED_WORLD_PVP_QUEUE || You are now queued for Ashran.
|-
| 797 ||  ||  || ERR_LFG_JOINED_BATTLEFIELD_QUEUE || You are now queued for Brawls.
|-
| 798 ||  ||  || ERR_LFG_JOINED_LIST || You are now listed for Other Raids.
|-
| 799 ||  ||  || ERR_LFG_LEFT_QUEUE || You are no longer queued.
|-
| 800 ||  ||  || ERR_LFG_LEFT_LIST || You are no longer listed for Other Raids.
|-
| 801 ||  ||  || ERR_LFG_ROLE_CHECK_ABORTED || Your group leader has canceled the Role Check.
|-
| 802 ||  ||  || ERR_LFG_READY_CHECK_ABORTED || Your group leader has canceled the Ready Check.
|-
| 803 ||  ||  || ERR_LFG_CANT_USE_BATTLEGROUND || You cannot queue for a battleground or arena while using the dungeon or raid queueing systems.
|-
| 804 ||  ||  || ERR_LFG_CANT_USE_DUNGEONS || You cannot queue for a dungeon or raid while using battlegrounds or arenas.
|-
| 805 ||  ||  || ERR_LFG_REASON_TOO_MANY_LFG || You are queued for too many instances.
|-
| 806 ||  ||  || ERR_LFG_FARM_LIMIT || You or someone in your party has entered too many instances recently. Please wait awhile and try again.
|-
| 807 ||  ||  || ERR_LFG_NO_CROSS_FACTION_PARTIES || Cross-faction groups can't queue for this instance
|-
| 808 ||  ||  || ERR_INVALID_TELEPORT_LOCATION || You do not have a valid teleport location.
|-
| 809 ||  ||  || ERR_TOO_FAR_TO_INTERACT || You need to be closer to interact with that target.
|-
| 810 ||  ||  || ERR_BATTLEGROUND_PLAYERS_FROM_DIFFERENT_REALMS || You cannot queue for a battleground while players from different realms are in your party.
|-
| 811 ||  ||  || ERR_DIFFICULTY_CHANGE_COOLDOWN_S || Raid difficulty has changed recently, and may not change again for %s.
|-
| 812 ||  ||  || ERR_DIFFICULTY_CHANGE_COMBAT_COOLDOWN_S || Raid was in combat recently and may not change difficulty again for %s.
|-
| 813 ||  ||  || ERR_DIFFICULTY_CHANGE_WORLDSTATE || Raid difficulty cannot be changed at this time. An event is in progress.
|-
| 814 ||  ||  || ERR_DIFFICULTY_CHANGE_ENCOUNTER || Raid difficulty cannot be changed at this time. An encounter is in progress.
|-
| 815 ||  ||  || ERR_DIFFICULTY_CHANGE_COMBAT || Raid difficulty cannot be changed at this time. A player is in combat.
|-
| 816 ||  ||  || ERR_DIFFICULTY_CHANGE_PLAYER_BUSY || Raid difficulty cannot be changed at this time. A player is busy.
|-
| 817 ||  ||  || ERR_DIFFICULTY_CHANGE_ALREADY_STARTED || A raid difficulty change is currently in progress.
|-
| 818 ||  ||  || ERR_DIFFICULTY_CHANGE_OTHER_HEROIC_S || Raid difficulty cannot be changed. %s is already locked to a different Heroic instance.
|-
| 819 ||  ||  || ERR_DIFFICULTY_CHANGE_HEROIC_INSTANCE_ALREADY_RUNNING || Your heroic instance is already in running and in use by another party
|-
| 820 ||  ||  || ERR_ARENA_TEAM_PARTY_SIZE || Incorrect party size for this arena.
|-
| 821 ||  ||  || ERR_SOLO_SHUFFLE_WARGAME_GROUP_SIZE || Exactly 6 non-spectator players must be present to begin a Solo Shuffle Wargame.
|-
| 822 ||  ||  || ERR_SOLO_SHUFFLE_WARGAME_GROUP_COMP || Exactly 4 DPS, and either 2 Tanks or 2 Healers, must be present to begin a Solo Shuffle Wargame.
|-
| 823 ||  ||  || ERR_PVP_PLAYER_ABANDONED || A player has abandoned the match, and will receive a queue penalty.
|-
| 824 ||  ||  || ERR_QUEST_FORCE_REMOVED_S || The quest %s has been removed from your quest log.
|-
| 825 ||  ||  || ERR_ATTACK_NO_ACTIONS || Can't attack while actions are prevented.
|-
| 826 ||  ||  || ERR_IN_RANDOM_BG || Can't do that while in a Random Battleground queue.
|-
| 827 ||  ||  || ERR_IN_NON_RANDOM_BG || Can't queue for Random Battleground while in another Battleground queue.
|-
| 828 ||  ||  || ERR_BN_FRIEND_SELF || You can't put yourself on your friend list
|-
| 829 ||  ||  || ERR_BN_FRIEND_ALREADY || That person is already your friend
|-
| 830 ||  ||  || ERR_BN_FRIEND_BLOCKED || That person is on your blocked list
|-
| 831 ||  ||  || ERR_BN_FRIEND_LIST_FULL || You don't have room for any more Blizzard friends.
|-
| 832 ||  ||  || ERR_BN_FRIEND_REQUEST_SENT || Friend request has been sent
|-
| 833 ||  ||  || ERR_BN_BROADCAST_THROTTLE || Please wait a few seconds before updating your broadcast message again.
|-
| 834 ||  ||  || ERR_BG_DEVELOPER_ONLY || This battleground is only available for developer testing at this time.
|-
| 835 ||  ||  || ERR_CURRENCY_SPELL_SLOT_MISMATCH || That item can't be used in that slot
|-
| 836 ||  ||  || ERR_CURRENCY_NOT_TRADABLE || 
|-
| 837 ||  ||  || ERR_REQUIRES_EXPANSION_S || Requires expansion: %s
|-
| 838 || 847 ||  || ERR_QUEST_FAILED_SPELL || You haven't learned the required spell.
|-
| 839 ||  ||  || ERR_TALENT_FAILED_NOT_ENOUGH_TALENTS_IN_PRIMARY_TREE || You need to spend more talents in your primary talent tree before you can put points here.
|-
| 840 ||  ||  || ERR_TALENT_FAILED_NO_PRIMARY_TREE_SELECTED || Please select a primary talent tree before spending talents.
|-
| 841 ||  ||  || ERR_TALENT_FAILED_CANT_REMOVE_TALENT || You can't change that talent choice while %s is on cooldown.
|-
| 842 ||  ||  || ERR_TALENT_FAILED_UNKNOWN || Unable to learn talent.
|-
| 843 ||  ||  || ERR_WARGAME_REQUEST_FAILURE || War Game request failed
|-
| 844 ||  ||  || ERR_RANK_REQUIRES_AUTHENTICATOR || Guild rank requires an authenticator.
|-
| 845 ||  ||  || ERR_GUILD_BANK_VOUCHER_FAILED || You must purchase all guild bank tabs before using this voucher.
|-
| 846 || 888 ||  || ERR_WARGAME_REQUEST_SENT || Your War Game request has been sent.
|-
| 847 ||  ||  || ERR_REQUIRES_ACHIEVEMENT_I || 
|-
| 848 ||  ||  || ERR_REFUND_RESULT_EXCEED_MAX_CURRENCY || Cannot grant a currency refund exceeding the maximum allowed amount.
|-
| 849 ||  ||  || ERR_CANT_BUY_QUANTITY || You can't buy the specified quantity of that item.
|-
| 850 ||  ||  || ERR_ITEM_IS_BATTLE_PAY_LOCKED || Your purchased item is still waiting to be unlocked
|-
| 851 ||  ||  || ERR_PARTY_ALREADY_IN_BATTLEGROUND_QUEUE || Player is already in a battleground queue.
|-
| 852 ||  ||  || ERR_PARTY_CONFIRMING_BATTLEGROUND_QUEUE || The party is already confirming a battleground queue.
|-
| 853 ||  ||  || ERR_BATTLEFIELD_TEAM_PARTY_SIZE || Incorrect party size for this battlefield.
|-
| 854 ||  ||  || ERR_INSUFF_TRACKED_CURRENCY_IS || You must earn %d more %s for the season in order to purchase that item.
|-
| 855 ||  ||  || ERR_NOT_ON_TOURNAMENT_REALM || Not available on a Tournament Realm.
|-
| 856 ||  ||  || ERR_GUILD_TRIAL_ACCOUNT_TRIAL || Free Trial accounts cannot join guilds.
|-
| 857 ||  ||  || ERR_GUILD_TRIAL_ACCOUNT_VETERAN || This account cannot join guilds without an existing character in the guild.
|-
| 858 ||  ||  || ERR_GUILD_UNDELETABLE_DUE_TO_LEVEL || Your guild is too high level to be deleted.
|-
| 859 ||  ||  || ERR_CANT_DO_THAT_IN_A_GROUP || You can't do that while in a group.
|-
| 860 ||  ||  || ERR_GUILD_LEADER_REPLACED || Because the previous guild master %s has not logged in for an extended time, %s has become the new Guild Master.
|-
| 861 ||  ||  || ERR_TRANSMOGRIFY_CANT_EQUIP || You must be able to equip an item to use its appearance.
|-
| 862 ||  ||  || ERR_TRANSMOGRIFY_INVALID_ITEM_TYPE || This item does not have a valid appearance.
|-
| 863 ||  ||  || ERR_TRANSMOGRIFY_NOT_SOULBOUND || %s cannot be transmogrified because it is not permanently bound to you.
|-
| 864 ||  ||  || ERR_TRANSMOGRIFY_INVALID_SOURCE || This item's appearance cannot be used.
|-
| 865 ||  ||  || ERR_TRANSMOGRIFY_INVALID_DESTINATION || %s cannot be transmogrified.
|-
| 866 ||  ||  || ERR_TRANSMOGRIFY_MISMATCH || You can only transmogrify an item to take the appearance of an item of the same type and slot.
|-
| 867 ||  ||  || ERR_TRANSMOGRIFY_LEGENDARY || You cannot transmogrify or use the appearance of a legendary item.
|-
| 868 ||  ||  || ERR_TRANSMOGRIFY_SAME_ITEM || You cannot transmogrify an item with the same item.
|-
| 869 ||  ||  || ERR_TRANSMOGRIFY_SAME_APPEARANCE || %s already has that appearance.
|-
| 870 ||  ||  || ERR_TRANSMOGRIFY_NOT_EQUIPPED || 
|-
| 871 ||  ||  || ERR_VOID_DEPOSIT_FULL || You can't deposit more than 9 items at once.
|-
| 872 ||  ||  || ERR_VOID_WITHDRAW_FULL || You can't withdraw more than 9 items at once.
|-
| 873 ||  ||  || ERR_VOID_STORAGE_WRAPPED || You cannot deposit wrapped items in void storage.
|-
| 874 ||  ||  || ERR_VOID_STORAGE_STACKABLE || You cannot deposit stackable items in void storage.
|-
| 875 ||  ||  || ERR_VOID_STORAGE_UNBOUND || Only soulbound items can be deposited in void storage.
|-
| 876 ||  ||  || ERR_VOID_STORAGE_REPAIR || You must repair that item before you can deposit it in void storage.
|-
| 877 ||  ||  || ERR_VOID_STORAGE_CHARGES || You cannot deposit an item with used charges in void storage.
|-
| 878 ||  ||  || ERR_VOID_STORAGE_QUEST || You cannot deposit quest items in void storage.
|-
| 879 ||  ||  || ERR_VOID_STORAGE_CONJURED || You cannot deposit conjured items in void storage.
|-
| 880 ||  ||  || ERR_VOID_STORAGE_MAIL || You cannot deposit mail items in void storage.
|-
| 881 ||  ||  || ERR_VOID_STORAGE_BAG || You cannot deposit a non-empty bag in void storage.
|-
| 882 ||  ||  || ERR_VOID_TRANSFER_STORAGE_FULL || There is not enough room in void storage to complete the deposit.
|-
| 883 ||  ||  || ERR_VOID_TRANSFER_INV_FULL || There is not enough room in your bags to complete the withdrawal.
|-
| 884 ||  ||  || ERR_VOID_TRANSFER_INTERNAL_ERROR || Internal void storage error.
|-
| 885 ||  ||  || ERR_VOID_TRANSFER_ITEM_INVALID || One or more of your items are ineligible to be deposited into void storage.
|-
| 886 ||  ||  || ERR_DIFFICULTY_DISABLED_IN_LFG || Using Raid Finder to enter this instance disables dynamic difficulty selection
|-
| 887 ||  ||  || ERR_VOID_STORAGE_UNIQUE || You cannot deposit unique items in void storage.
|-
| 888 ||  ||  || ERR_VOID_STORAGE_LOOT || You cannot deposit lootable items in void storage.
|-
| 889 ||  ||  || ERR_VOID_STORAGE_HOLIDAY || You cannot deposit Holiday related items in void storage.
|-
| 890 ||  ||  || ERR_VOID_STORAGE_DURATION || You cannot deposit items with limited duration in void storage.
|-
| 891 ||  ||  || ERR_VOID_STORAGE_LOAD_FAILED || Failed to load void storage items.
|-
| 892 ||  ||  || ERR_VOID_STORAGE_INVALID_ITEM || You cannot deposit that item into void storage.
|-
| 893 ||  ||  || ERR_PARENTAL_CONTROLS_CHAT_MUTED || Chat is disabled due to your Battle.net Account parental controls or privacy settings
|-
| 894 ||  ||  || ERR_SOR_START_EXPERIENCE_INCOMPLETE || 
|-
| 895 ||  ||  || ERR_SOR_INVALID_EMAIL || That email address is invalid.
|-
| 896 ||  ||  || ERR_SOR_INVALID_COMMENT || That comment has invalid characters.
|-
| 897 ||  ||  || ERR_CHALLENGE_MODE_RESET_COOLDOWN_S || Instance can not be reset for another %s.
|-
| 898 ||  ||  || ERR_CHALLENGE_MODE_RESET_KEYSTONE || You may not reset a Mythic dungeon that was started with an energized Keystone. Complete the dungeon to claim your rewards.
|-
| 899 ||  ||  || ERR_PET_JOURNAL_ALREADY_IN_LOADOUT || That pet is already in your loadout.
|-
| 900 ||  ||  || ERR_REPORT_SUBMITTED_SUCCESSFULLY || Thank you for your report!
|-
| 901 ||  ||  || ERR_REPORT_SUBMISSION_FAILED || Report system unavailable.
|-
| 902 ||  ||  || ERR_SUGGESTION_SUBMITTED_SUCCESSFULLY || Suggestion Submitted!
|-
| 903 ||  ||  || ERR_BUG_SUBMITTED_SUCCESSFULLY || Bug Submitted!
|-
| 904 ||  ||  || ERR_CHALLENGE_MODE_ENABLED || Challenge Mode enabled.
|-
| 905 ||  ||  || ERR_CHALLENGE_MODE_DISABLED || Challenge Mode disabled.
|-
| 906 ||  ||  || ERR_PETBATTLE_CREATE_FAILED || Failed to create pet battle.
|-
| 907 ||  ||  || ERR_PETBATTLE_NOT_HERE || Cannot pet battle here.
|-
| 908 ||  ||  || ERR_PETBATTLE_NOT_HERE_ON_TRANSPORT || Cannot pet battle on a transport.
|-
| 909 ||  ||  || ERR_PETBATTLE_NOT_HERE_UNEVEN_GROUND || Ground is too uneven to pet battle.
|-
| 910 ||  ||  || ERR_PETBATTLE_NOT_HERE_OBSTRUCTED || Pet battle area is obstructed.
|-
| 911 ||  ||  || ERR_PETBATTLE_NOT_WHILE_IN_COMBAT || Cannot pet battle while in combat.
|-
| 912 ||  ||  || ERR_PETBATTLE_NOT_WHILE_DEAD || Cannot pet battle while dead.
|-
| 913 ||  ||  || ERR_PETBATTLE_NOT_WHILE_FLYING || Must be standing to pet battle.
|-
| 914 ||  ||  || ERR_PETBATTLE_TARGET_INVALID || Not a valid pet battle target.
|-
| 915 ||  ||  || ERR_PETBATTLE_TARGET_OUT_OF_RANGE || Pet battle target out of range.
|-
| 916 ||  ||  || ERR_PETBATTLE_TARGET_NOT_CAPTURABLE || Creature is not a valid pet battle target.
|-
| 917 ||  ||  || ERR_PETBATTLE_NOT_A_TRAINER || Must be a battle pet trainer to pet battle.
|-
| 918 ||  ||  || ERR_PETBATTLE_DECLINED || Pet battle invitation declined.
|-
| 919 ||  ||  || ERR_PETBATTLE_IN_BATTLE || Pet battle already in progress.
|-
| 920 ||  ||  || ERR_PETBATTLE_INVALID_LOADOUT || You must equip a pet in a pet battle slot.
|-
| 921 ||  ||  || ERR_PETBATTLE_ALL_PETS_DEAD || All pets in your battle slots are dead.
|-
| 922 ||  ||  || ERR_PETBATTLE_NO_PETS_IN_SLOTS || Must have a pet in battle slot.
|-
| 923 ||  ||  || ERR_PETBATTLE_NO_ACCOUNT_LOCK || Pet Journal Is Locked by another user on this account
|-
| 924 ||  ||  || ERR_PETBATTLE_WILD_PET_TAPPED || Pet is being battled by another player.
|-
| 925 ||  ||  || ERR_PETBATTLE_RESTRICTED_ACCOUNT || Free Trial accounts can't participate in pet battles.
|-
| 926 ||  ||  || ERR_PETBATTLE_OPPONENT_NOT_AVAILABLE || Your pet battle opponent is no longer available.
|-
| 927 ||  ||  || ERR_PETBATTLE_NOT_WHILE_IN_MATCHED_BATTLE || You can't do that in a matched pet battle.
|-
| 928 ||  ||  || ERR_CANT_HAVE_MORE_PETS_OF_THAT_TYPE || You can't have any more pets of that type.
|-
| 929 ||  ||  || ERR_CANT_HAVE_MORE_PETS || You can't have any more pets.
|-
| 930 ||  ||  || ERR_PVP_MAP_NOT_FOUND || Blacklisted map not set.
|-
| 931 ||  ||  || ERR_PVP_MAP_NOT_SET || Failed to blacklist PvP map.
|-
| 932 ||  ||  || ERR_PETBATTLE_QUEUE_QUEUED || You are now queued for a pet battle.
|-
| 933 ||  ||  || ERR_PETBATTLE_QUEUE_ALREADY_QUEUED || You are already queued for a pet battle.
|-
| 934 ||  ||  || ERR_PETBATTLE_QUEUE_JOIN_FAILED || Unable to join pet battle queue.
|-
| 935 ||  ||  || ERR_PETBATTLE_QUEUE_JOURNAL_LOCK || Pet Journal unavailable for battle.
|-
| 936 ||  ||  || ERR_PETBATTLE_QUEUE_REMOVED || You are no longer in the pet battle queue.
|-
| 937 ||  ||  || ERR_PETBATTLE_QUEUE_PROPOSAL_DECLINED || You declined the pet battle invitation.
|-
| 938 ||  ||  || ERR_PETBATTLE_QUEUE_PROPOSAL_TIMEOUT || You did not respond to the pet battle invitation.
|-
| 939 ||  ||  || ERR_PETBATTLE_QUEUE_OPPONENT_DECLINED || Opponent declined pet battle invitation. You have been returned to the queue.
|-
| 940 ||  ||  || ERR_PETBATTLE_QUEUE_REQUEUED_INTERNAL || Internal pet battle error. You have been re-queued for battle.
|-
| 941 ||  ||  || ERR_PETBATTLE_QUEUE_REQUEUED_REMOVED || Pet battle opponent unavailable. You have been re-queued for battle.
|-
| 942 ||  ||  || ERR_PETBATTLE_QUEUE_SLOT_LOCKED || Pet battle slot %d is locked.
|-
| 943 ||  ||  || ERR_PETBATTLE_QUEUE_SLOT_EMPTY || Pet battle slot %d is empty.
|-
| 944 ||  ||  || ERR_PETBATTLE_QUEUE_SLOT_NO_TRACKER || Pet battle slot %d is invalid.
|-
| 945 ||  ||  || ERR_PETBATTLE_QUEUE_SLOT_NO_SPECIES || 
|-
| 946 ||  ||  || ERR_PETBATTLE_QUEUE_SLOT_CANT_BATTLE || Pet in slot %d can't battle.
|-
| 947 ||  ||  || ERR_PETBATTLE_QUEUE_SLOT_REVOKED || Pet in slot %d is unavailable for battle.
|-
| 948 ||  ||  || ERR_PETBATTLE_QUEUE_SLOT_DEAD || Pet in slot %d is dead.
|-
| 949 ||  ||  || ERR_PETBATTLE_QUEUE_SLOT_NO_PET || Pet battle slot %d has no pet.
|-
| 950 ||  ||  || ERR_PETBATTLE_QUEUE_NOT_WHILE_NEUTRAL || Neutral characters cannot pet battle.
|-
| 951 ||  ||  || ERR_PETBATTLE_GAME_TIME_LIMIT_WARNING || Pet Battle Time Limit Reached - Will End in %d Minutes
|-
| 952 ||  ||  || ERR_PETBATTLE_GAME_ROUNDS_LIMIT_WARNING || Pet Battle Round Limit Reached - Will End in %d Rounds
|-
| 953 ||  ||  || ERR_HAS_RESTRICTION || That action is currently restricted.
|-
| 954 ||  ||  || ERR_ITEM_UPGRADE_ITEM_TOO_LOW_LEVEL || Item must be level 458 or higher
|-
| 955 ||  ||  || ERR_ITEM_UPGRADE_NO_PATH || Item cannot be upgraded
|-
| 956 ||  ||  || ERR_ITEM_UPGRADE_NO_MORE_UPGRADES || This item is fully upgraded
|-
| 957 ||  ||  || ERR_BONUS_ROLL_EMPTY || You were not eligible to receive any loot from this boss. You have not been charged for your bonus roll.
|-
| 958 ||  ||  || ERR_CHALLENGE_MODE_FULL || A maximum of five unique players may enter a Challenge instance. Resetting the instance also resets this counter.
|-
| 959 ||  ||  || ERR_CHALLENGE_MODE_IN_PROGRESS || You can't enter a Mythic+ dungeon that is in progress
|-
| 960 ||  ||  || ERR_CHALLENGE_MODE_INCORRECT_KEYSTONE || That keystone is for a different dungeon.
|-
| 961 ||  ||  || ERR_BATTLETAG_FRIEND_NOT_FOUND || Could not find target player.
|-
| 962 ||  ||  || ERR_BATTLETAG_FRIEND_NOT_VALID || Cannot send BattleTag friend requests to that player.
|-
| 963 ||  ||  || ERR_BATTLETAG_FRIEND_NOT_ALLOWED || You cannot send BattleTag friend requests.
|-
| 964 ||  ||  || ERR_BATTLETAG_FRIEND_THROTTLED || Cannot send BattleTag friend requests right now.
|-
| 965 ||  ||  || ERR_BATTLETAG_FRIEND_SUCCESS || BattleTag friend request has been sent.
|-
| 966 ||  ||  || ERR_PET_TOO_HIGH_LEVEL_TO_UNCAGE || This pet is too high level for you to uncage.
|-
| 967 ||  ||  || ERR_PETBATTLE_INTERNAL || Internal pet battle error.
|-
| 968 ||  ||  || ERR_CANT_CAGE_PET_YET || You can't cage this pet for another %d hours and %d minutes.
|-
| 969 ||  ||  || ERR_NO_LOOT_IN_CHALLENGE_MODE || You can't loot items while the Challenge is active.
|-
| 970 ||  ||  || ERR_QUEST_PET_BATTLE_VICTORIES_PVP_II || Players defeated in pet battle: %d/%d
|-
| 971 ||  ||  || ERR_ROLE_CHECK_ALREADY_IN_PROGRESS || A role check is already in progress.
|-
| 972 ||  ||  || ERR_RECRUIT_A_FRIEND_ACCOUNT_LIMIT || You have submitted the maximum number of recruits for this time period. Please try again later.
|-
| 973 ||  ||  || ERR_RECRUIT_A_FRIEND_FAILED || Failed to send Recruit A Friend request. Please try again later.
|-
| 974 ||  ||  || ERR_SET_LOOT_PERSONAL || Looting set to Personal.
|-
| 975 ||  ||  || ERR_SET_LOOT_METHOD_FAILED_COMBAT || Failed to change loot method: A party member is in combat.
|-
| 976 ||  ||  || ERR_REAGENT_BANK_FULL || Your reagent bank is full
|-
| 977 ||  ||  || ERR_REAGENT_BANK_LOCKED || 
|-
| 978 ||  ||  || ERR_GARRISON_BUILDING_EXISTS || Building exists.
|-
| 979 ||  ||  || ERR_GARRISON_INVALID_PLOT || Invalid plot.
|-
| 980 ||  ||  || ERR_GARRISON_INVALID_BUILDINGID || Invalid building ID.
|-
| 981 ||  ||  || ERR_GARRISON_INVALID_PLOT_BUILDING || That building can't go there.
|-
| 982 ||  ||  || ERR_GARRISON_REQUIRES_BLUEPRINT || Blueprint needed.
|-
| 983 ||  ||  || ERR_GARRISON_NOT_ENOUGH_CURRENCY || Not enough material to purchase building.
|-
| 984 ||  ||  || ERR_GARRISON_NOT_ENOUGH_GOLD || Not enough gold to purchase building.
|-
| 985 ||  ||  || ERR_GARRISON_COMPLETE_MISSION_WRONG_FOLLOWER_TYPE || You cannot complete this type of mission with that.
|-
| 986 ||  ||  || ERR_ALREADY_USING_LFG_LIST || You can't do that while using Premade Groups.
|-
| 987 ||  ||  || ERR_RESTRICTED_ACCOUNT_LFG_LIST_TRIAL || Free Trial accounts cannot use this feature.
|-
| 988 ||  ||  || ERR_TOY_USE_LIMIT_REACHED || Toy Use Limit Reached
|-
| 989 ||  ||  || ERR_TOY_ALREADY_KNOWN || 
|-
| 990 ||  ||  || ERR_TRANSMOG_SET_ALREADY_KNOWN || All appearances are already in your collection.
|-
| 991 ||  || 40 || ERR_NOT_ENOUGH_CURRENCY || You don't have enough currency to do that.
|-
| 992 ||  ||  || ERR_SPEC_IS_DISABLED || That spec is currently disabled
|-
| 993 ||  ||  || ERR_FEATURE_RESTRICTED_TRIAL || Feature not available for Free Trial accounts.
|-
| 994 ||  ||  || ERR_CANT_BE_OBLITERATED || You can't obliterate that item
|-
| 995 ||  ||  || ERR_CANT_BE_SCRAPPED || You can't scrap that item
|-
| 996 ||  ||  || ERR_ARTIFACT_RELIC_DOES_NOT_MATCH_ARTIFACT || This relic is not attuned for your equipped artifact
|-
| 997 ||  ||  || ERR_MUST_EQUIP_ARTIFACT || You must have an artifact equipped.
|-
| 998 ||  ||  || ERR_CANT_DO_THAT_RIGHT_NOW || You can't do that right now.
|-
| 999 ||  ||  || ERR_AFFECTING_COMBAT || You are in combat
|-
| 1000 ||  ||  || ERR_EQUIPMENT_MANAGER_COMBAT_SWAP_S || Some items from set %s cannot be swapped because you are in combat.
|-
| 1001 ||  ||  || ERR_EQUIPMENT_MANAGER_BAGS_FULL || Equipment swap failed. Inventory is full.
|-
| 1002 ||  ||  || ERR_EQUIPMENT_MANAGER_MISSING_ITEM_S || One or more items from set %s were missing and could not be equipped.
|-
| 1003 ||  ||  || ERR_MOVIE_RECORDING_WARNING_PERF || Recording stopped - the movie recording settings may be too high for this system configuration.
|-
| 1004 ||  ||  || ERR_MOVIE_RECORDING_WARNING_DISK_FULL || You don't have enough free space on your hard drive to record movies.
|-
| 1005 ||  ||  || ERR_MOVIE_RECORDING_WARNING_NO_MOVIE || There is no movie to compress.
|-
| 1006 ||  ||  || ERR_MOVIE_RECORDING_WARNING_REQUIREMENTS || 
|-
| 1007 ||  ||  || ERR_MOVIE_RECORDING_WARNING_COMPRESSING || You cannot start recording while compressing a movie.
|-
| 1008 ||  ||  || ERR_NO_CHALLENGE_MODE_REWARD || Complete a Mythic+ dungeon and return next week to claim your reward.
|-
| 1009 ||  ||  || ERR_CLAIMED_CHALLENGE_MODE_REWARD || You have already claimed your Challenger's Bounty for the week.
|-
| 1010 ||  ||  || ERR_CHALLENGE_MODE_PERIOD_RESET_SS || This instance will close at %s. (%s remaining)
|-
| 1011 ||  ||  || ERR_CANT_DO_THAT_CHALLENGE_MODE_ACTIVE || You can't do that while a Mythic Keystone is active
|-
| 1012 ||  ||  || ERR_TALENT_FAILED_REST_AREA || You must be in a rest area to change talents
|-
| 1013 ||  ||  || ERR_CANNOT_ABANDON_LAST_PET || Cannot Abandon Last Pet
|-
| 1014 ||  ||  || ERR_TEST_CVAR_SET_SSS || Test CVar %s has been set to %s (default %s)
|-
| 1015 ||  ||  || ERR_QUEST_TURN_IN_FAIL_REASON || %s
|-
| 1016 ||  ||  || ERR_CLAIMED_CHALLENGE_MODE_REWARD_OLD || You didn't complete a Mythic+ dungeon last week
|-
| 1017 ||  ||  || ERR_TALENT_GRANTED_BY_AURA || 
|-
| 1018 ||  ||  || ERR_CHALLENGE_MODE_ALREADY_COMPLETE || This Mythic+ dungeon has already been completed.
|-
| 1019 ||  ||  || ERR_GLYPH_TARGET_NOT_AVAILABLE || The target spell is currently overwritten by a talent or other ability.
|-
| 1020 ||  ||  || ERR_PVP_WARMODE_TOGGLE_ON || War Mode toggled on
|-
| 1021 ||  ||  || ERR_PVP_WARMODE_TOGGLE_OFF || War Mode toggled off
|-
| 1022 ||  ||  || ERR_SPELL_FAILED_LEVEL_REQUIREMENT || You are not high enough level
|-
| 1023 ||  ||  || ERR_BATTLEGROUND_JOIN_REQUIRES_LEVEL || Tournament rules requires all participants to be max level.
|-
| 1024 ||  ||  || ERR_BATTLEGROUND_JOIN_DISQUALIFIED || %s has been disqualified from ranked play in this bracket.
|-
| 1025 ||  ||  || ERR_BATTLEGROUND_JOIN_DISQUALIFIED_NO_NAME || A player has been disqualified from ranked play in this bracket.
|-
| 1026 ||  ||  || ERR_VOICE_CHAT_GENERIC_UNABLE_TO_CONNECT || Can't connect to a voice chat server right now. Please try again.
|-
| 1027 ||  ||  || ERR_VOICE_CHAT_SERVICE_LOST || Lost connection to the voice chat service.
|-
| 1028 ||  ||  || ERR_VOICE_CHAT_CHANNEL_NAME_TOO_SHORT || You must provide a name for the channel.
|-
| 1029 ||  ||  || ERR_VOICE_CHAT_CHANNEL_NAME_TOO_LONG || Maximum channel name length is 30 characters.
|-
| 1030 ||  ||  || ERR_VOICE_CHAT_CHANNEL_ALREADY_EXISTS || You're already a member of a channel with that name.
|-
| 1031 ||  ||  || ERR_VOICE_CHAT_TARGET_NOT_FOUND || Could not find the player to invite to to the voice chat channel.
|-
| 1032 ||  ||  || ERR_VOICE_CHAT_TOO_MANY_REQUESTS || Waiting to hear back from the voice chat server. Please try again in a minute.
|-
| 1033 ||  ||  || ERR_VOICE_CHAT_PLAYER_SILENCED || We have silenced your account following multiple reports of abusive chat from other players. While you are silenced, you can only use voice chat in private channels.
|-
| 1034 ||  ||  || ERR_VOICE_CHAT_PARENTAL_DISABLE_ALL || Voice Chat has been disabled by Parental Controls.
|-
| 1035 ||  ||  || ERR_VOICE_CHAT_DISABLED || Voice Chat has been temporarily disabled.
|-
| 1036 ||  ||  || ERR_NO_PVP_REWARD || Earn Conquest points through Rated PvP and return next week to claim your reward.
|-
| 1037 ||  ||  || ERR_CLAIMED_PVP_REWARD || You have already claimed your Conqueror's Spoils for the week.
|-
| 1038 ||  ||  || ERR_AZERITE_ESSENCE_SELECTION_FAILED_ESSENCE_NOT_UNLOCKED || %s hasn't been unlocked yet
|-
| 1039 ||  ||  || ERR_AZERITE_ESSENCE_SELECTION_FAILED_CANT_REMOVE_ESSENCE || You can't change that Essence while %s is on cooldown
|-
| 1040 ||  ||  || ERR_AZERITE_ESSENCE_SELECTION_FAILED_CONDITION_FAILED || You don't meet the requirements to apply this Essence
|-
| 1041 ||  ||  || ERR_AZERITE_ESSENCE_SELECTION_FAILED_REST_AREA || You must be in a rest area to change Essences
|-
| 1042 ||  ||  || ERR_AZERITE_ESSENCE_SELECTION_FAILED_SLOT_LOCKED || You haven't unlocked this Essence slot yet
|-
| 1043 ||  ||  || ERR_AZERITE_ESSENCE_SELECTION_FAILED_NOT_AT_FORGE || You must be at the Heart Forge to do that
|-
| 1044 ||  ||  || ERR_AZERITE_ESSENCE_SELECTION_FAILED_HEART_LEVEL_TOO_LOW || Requires Heart of Azeroth level %d
|-
| 1045 ||  ||  || ERR_AZERITE_ESSENCE_SELECTION_FAILED_NOT_EQUIPPED || Must have the %s equipped
|-
| 1046 ||  ||  || ERR_SOCKETING_REQUIRES_PUNCHCARDRED_GEM || That slot requires a Red Punchcard.
|-
| 1047 ||  ||  || ERR_SOCKETING_PUNCHCARDRED_GEM_ONLY_IN_PUNCHCARDREDSLOT || Red Punchcards can only be placed in Red Punchcard sockets.
|-
| 1048 ||  ||  || ERR_SOCKETING_REQUIRES_PUNCHCARDYELLOW_GEM || That slot requires a Yellow Punchcard.
|-
| 1049 ||  ||  || ERR_SOCKETING_PUNCHCARDYELLOW_GEM_ONLY_IN_PUNCHCARDYELLOWSLOT || Yellow Punchcards can only be placed in Yellow Punchcard sockets.
|-
| 1050 ||  ||  || ERR_SOCKETING_REQUIRES_PUNCHCARDBLUE_GEM || That slot requires a Blue Punchcard.
|-
| 1051 ||  ||  || ERR_SOCKETING_PUNCHCARDBLUE_GEM_ONLY_IN_PUNCHCARDBLUESLOT || Blue Punchcards can only be placed in Blue Punchcard sockets.
|-
| 1052 ||  ||  || ERR_SOCKETING_REQUIRES_DOMINATION_SHARD || That slot requires a Shard of Domination.
|-
| 1053 ||  ||  || ERR_SOCKETING_DOMINATION_SHARD_ONLY_IN_DOMINATIONSLOT || Shards of Domination can only be placed in Domination sockets.
|-
| 1054 ||  ||  || ERR_SOCKETING_REQUIRES_CYPHER_GEM || That slot requires a Crystallic Spheroid.
|-
| 1055 ||  ||  || ERR_SOCKETING_CYPHER_GEM_ONLY_IN_CYPHERSLOT || Crystallic Spheroids can only be placed in Crystallic sockets.
|-
| 1056 ||  ||  || ERR_LEVEL_LINKING_RESULT_LINKED || Your level is now restricted to %d.
|-
| 1057 ||  ||  || ERR_LEVEL_LINKING_RESULT_UNLINKED || Your level is no longer restricted.
|-
| 1058 ||  ||  || ERR_CLUB_FINDER_ERROR_POST_CLUB || Couldn't post at this time. Try again later.
|-
| 1059 ||  ||  || ERR_CLUB_FINDER_ERROR_APPLY_CLUB || Couldn't apply. Try again later.
|-
| 1060 ||  ||  || ERR_CLUB_FINDER_ERROR_RESPOND_APPLICANT || Couldn't respond to applicant. Try again later.
|-
| 1061 ||  ||  || ERR_CLUB_FINDER_ERROR_CANCEL_APPLICATION || Couldn't cancel application. Try again later.
|-
| 1062 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_ACCEPT_APPLICATION || 
|-
| 1063 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_NO_INVITE_PERMISSIONS || You do not have permission to invite.
|-
| 1064 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_NO_POSTING_PERMISSIONS || You do not have permission to post.
|-
| 1065 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_APPLICANT_LIST || Applicant list could not be fetched do to a bnet error.
|-
| 1066 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_APPLICANT_LIST_NO_PERM || You do not have permission to view the applicant list.
|-
| 1067 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_FINDER_NOT_AVAILABLE || Finder is not available at this time.
|-
| 1068 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_GET_POSTING_IDS || Couldn't fetch posting ids.
|-
| 1069 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_JOIN_APPLICATION || Couldn't create an application for the posting.
|-
| 1070 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_REALM_NOT_ELIGIBLE || You cannot apply to guilds from a different realm.
|-
| 1071 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_FLAGGED_RENAME || Your %s has been flagged for a rename. Please enter a new name before updating the posting.
|-
| 1072 ||  ||  || ERR_CLUB_FINDER_ERROR_TYPE_FLAGGED_DESCRIPTION_CHANGE || Your %s description has been flagged as inappropriate. Please enter a new description before updating the posting.
|-
| 1073 ||  ||  || ERR_ITEM_INTERACTION_NOT_ENOUGH_GOLD || Not enough gold.
|-
| 1074 ||  ||  || ERR_ITEM_INTERACTION_NOT_ENOUGH_CURRENCY || Not enough %s.
|-
| 1075 ||  ||  || ERR_PLAYER_CHOICE_ERROR_PENDING_CHOICE || You have an unselected choice already. Please select a choice to open a new one.
|-
| 1076 ||  ||  || ERR_SOULBIND_INVALID_CONDUIT || Invalid Conduit
|-
| 1077 ||  ||  || ERR_SOULBIND_INVALID_CONDUIT_ITEM || Invalid Item
|-
| 1078 ||  ||  || ERR_SOULBIND_INVALID_TALENT || Invalid Talent
|-
| 1079 ||  ||  || ERR_SOULBIND_DUPLICATE_CONDUIT || You can't use the same Conduit twice. Right click an existing Conduit to remove it.
|-
| 1080 ||  ||  || ERR_ACTIVATE_SOULBIND_S || Soulbound with %s.
|-
| 1081 ||  ||  || ERR_ACTIVATE_SOULBIND_FAILED_REST_AREA || You must be in a rest area to change your Soulbind
|-
| 1082 ||  ||  || ERR_CANT_USE_PROFANITY || Can't use profanity.
|-
| 1083 ||  ||  || ERR_NOT_IN_PET_BATTLE || You cannot do that while in a pet battle
|-
| 1084 ||  ||  || ERR_NOT_IN_NPE || Not available during the tutorial
|-
| 1085 ||  ||  || ERR_NO_SPEC || You have not chosen a class specialization.
|-
| 1086 ||  ||  || ERR_NO_DOMINATIONSHARD_OVERWRITE || Shards of Domination can only be removed by the Soulfire Chisel
|-
| 1087 ||  ||  || ERR_USE_WEEKLY_REWARDS_DISABLED || The Great Vault is currently unavailable.
|-
| 1088 ||  ||  || ERR_CROSS_FACTION_GROUP_JOINED || This is now a cross-faction instance group. You can do these activities together: dungeons and raids (non-queued), Torghast, Rated PvP
|-
| 1089 ||  ||  || ERR_CANT_TARGET_UNFRIENDLY_IN_OVERWORLD || You can't target this player outside of an instance
|}</onlyinclude>

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```