# Category:API functions/Removed

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|notitle=1|nocat=1}}
Functions in this category have been removed from the [[API]] in a previous patch.  Some functions did not have pages defined before they were removed.

[[Category:Removed from World of Warcraft]]
[[Category:API functions| Removed]]

<!--  the list below should be eliminated as articles are properly created -->

===Arena Functions===
: [[API GetArenaCurrency|GetArenaCurrency]]() - Gets the amount of arena points a player currently has to spend. See [[API GetCurrencyInfo|GetCurrencyInfo]]() instead
: [[API IsBattlefieldArena|IsBattlefieldArena]]() - Returns true if the battlemaster you're talking to can queue you for arenas

===Auction Functions===
: [[API GetAuctionInvTypes|GetAuctionInvTypes]](classIndex, subclassIndex) - (7.0.3 Returns types of subcategories items.
: [[API GetAuctionItemClasses|GetAuctionItemClasses]]() - (7.0.3) Returns major auction item categories.

===Bag Functions===
: [[API QuestBagButtonIDToInvSlotID|QuestBagButtonIDToInvSlotID]](buttonID) - Possibly for a virtual bag to display quest items in.
: [[API SetBagPortaitTexture|SetBagPortaitTexture]](texture,slot) - Used to override the texture of a bag.

===Battleground Functions===
: [[API CloseBattlefield|CloseBattlefield]]() - (4.0) Closes the queue for battlefield window.
: [[API GetBattlefieldInfo|GetBattlefieldInfo]](index) - (4.0) Returns detailed information on the Battlefield you last opened a queue window for.
: [[API GetBattlefieldInstanceInfo|GetBattlefieldInstanceInfo]](index) - (4.0) Get the instance ID for a battlefield.
: [[API GetBattlefieldWorldStateUIInfo|GetBattlefieldWorldStateUIInfo]](index) &nbsp; - Get score and flag status within a battlefield. &nbsp; - Removed in 1.12
: [[API GetHonorCurrency|GetHonorCurrency]]() - (4.0) Gets the amount of honor points the player currently has to spend.  See [[API GetCurrencyInfo|GetCurrencyInfo]]() instead
: [[API GetNumBattlefields|GetNumBattlefields]]() - (4.0) Get the number of running battlefields for the last battleground queue window you opened.
: [[API GetNumBattlefieldWorldStateUI|GetNumBattlefieldWorldStateUI]]() &nbsp; - Get the number of World State UI Info available. &nbsp; - Removed in 1.12
: [[API GetSelectedBattlefield|GetSelectedBattlefield]]() - (4.0) Get the selected battlefield to join first.
: [[API SetSelectedBattlefield|SetSelectedBattlefield]](index) - (4.0) Select the battlefield instance you want to join or the first one that becomes available.
: [[API ShowBattlefieldList|ShowBattlefieldList]](index) - (3.3.3) Displays a queue window for the specified battlefield. Only works if you are already in a queue for the battlefield. Index corresponds to location in queue array.

===Character Functions===
: [[API GetRuneType|GetRuneType]](id) - (7.0.3) Returns the type of rune with the given id.

===Character Screen Functions===
: [[API CollapseAllHeaders|CollapseAllHeaders]]() (Removed in 3.1.0; possibly in favour of CollapseAllFactionHeaders)
: [[API ExpandAllHeaders|ExpandAllHeaders]]() (Removed in 3.1.0; possible in favour of ExpandAllFactionHeaders)
: [[API GetDamageBonusStat|GetDamageBonusStat]]() - (4.0) Returns index of which stat a player receives a damage bonus from increasing
: [[API IsTabViewable|IsTabViewable]](tab) - Returns true if specified tab is viewable by player, false otherwise
: [[API SetInventoryPortraitTexture|SetInventoryPortaitTexture]] - Set the texture to display in the Inventory (character) screen.

===Character Statistics Functions===
: [[API GetArmorPenetration|GetArmorPenetration]]() - (5.0) Returns percent of armor ignored by your physical attacks.
: [[API GetCritChanceFromAgility|GetCritChanceFromAgility]]("unit") - (7.0) Returns the amount of your critical hit chance contributed by Agility.
: [[API GetSpellCritChanceFromIntellect|GetSpellCritChanceFromIntellect]]("unit") - (7.0)

===Chat Frame Functions===
: [[API ChatFrameLog|ChatFrameLog]]() - (1.7) Obsolete

===Container/Bag Functions===
: [[API GetContainerItemGems|GetContainerItemGems]](bag, slot) - (7.0.3) Returns item IDs of gems inserted into the item in a specified container slot.
: [[API HasKey|HasKey]]() - (4.2.0) Returns 1 if the player has a keyring, nil otherwise.

===Crafting Functions===
Crafting API was absorbed into the TradeSkill API in 3.0. The following functions were not documented at the time of removal:

: [[API CloseCraft|CloseCraft]]()
: [[API CollapseCraftSkillLine|CollapseCraftSkillLine]](index)
: [[API DoCraft|DoCraft]](index)
: [[API ExpandCraftSkillLine|ExpandCraftSkillLine]](index)
: [[API GetCraftButtonToken|GetCraftButtonToken]]()
: [[API GetCraftCooldown|GetCraftCooldown]](index) - Returns the number of seconds left for a skill to cooldown.
: [[API GetCraftIcon|GetCraftIcon]](index)
: [[API GetCraftSelectionIndex|GetCraftSelectionIndex]]()
: [[API SelectCraft|SelectCraft]](index)

===Debugging Functions===
: [[API GetDebugStats|GetDebugStats]]()

===Glyph Functions===
: [[API CastGlyph|CastGlyph]](glyphID, slot) - (7.0.3)
: PROTECTED [[API CastGlyphByID|CastGlyphByID]] (glyphID, slot) - (7.0.3)
: PROTECTED [[API CastGlyphByName|CastGlyphByName]] (glyphName, slot) - (7.0.3)
: [[API GetGlyphClearInfo|GetGlyphClearInfo]]() - (7.0.3) Returns information about the current cost of removing a glyph.
: [[API GetGlyphInfo|GetGlyphInfo]](index) - (7.0.3) Returns details of the selected Glyph in the current players Glyph list
: [[API GetGlyphLink|GetGlyphLink]]([[Glyph SocketID|socketID]][, talentGroup]) - (7.0.3) Returns link text for a Glyph in the desired Socket.
: [[API GetGlyphLinkByID|GetGlyphLinkByID]](glyphID) - (7.0.3)
: [[API GetGlyphSocketInfo|GetGlyphSocketInfo]]([[Glyph SocketID|socketID]][, talentGroup]) - (7.0.3) Returns info on a specific Glyph Socket.
: [[API GetNumGlyphSockets|GetNumGlyphSockets]]() - (7.0.3) Returns the number of Glyph Sockets available at max level. (Same result as NUM_GLYPH_SLOTS)
: [[API GetNumGlyphs|GetNumGlyphs]]() - (7.0.3) Get the number of glyphs available for the character's class.
: [[API GetSelectedGlyphSpellIndex|GetSelectedGlyphSpellIndex]]() - (7.0.3)
: [[API GlyphMatchesSocket|GlyphMatchesSocket]]([[Glyph SocketID|socketID]]) - (7.0.3) See if the Glyph held by the cursor matches the desired Socket.
: [[API IsGlyphFlagSet|IsGlyphFlagSet]](filter) - (7.0.3) Returns the current state of the selected Glyph filter
: [[API PlaceGlyphInSocket|PlaceGlyphInSocket]]([[Glyph SocketID|socketID]]) - (7.0.3) Places the Glyph held by the cursor into the desired Socket.
: [[API RemoveGlyphFromSocket|RemoveGlyphFromSocket]]([[Glyph SocketID|socketID]]) - (7.0.3) Removes the Glyph from the desired Socket.
: [[API SetGlyphFilter|SetGlyphFilter]]() - (7.0.3)
: [[API SetGlyphNameFilter|SetGlyphNameFilter]](string) - (7.0.3)
: [[API SpellCanTargetGlyph|SpellCanTargetGlyph]]() - (7.0.3)
: [[API ToggleGlyphFilter|ToggleGlyphFilter]](filter) - (7.0.3) Toggles the state of the selected Glyph filter

===Guild Functions===
: [[API GetGuildBankWithdrawLimit|GetGuildBankWithdrawLimit]]() - (4.0) Returns withdraw limit for currently selected rank in guild control.  Renamed to [[API GetGuildBankWithdrawGoldLimit|GetGuildBankWithdrawGoldLimit]]
: [[API GetGuildRosterContribution|GetGuildRosterContribution]](index) - (6.0.2) Returns weekly and total XP as well as weekly and total rank.
: [[API GetGuildRosterLargestContribution|GetGuildRosterLargestContribution]]() - (6.0.2) Returns max weekly XP and max total XP.
: [[API GuildSetLeaderByName|GuildSetLeaderByName]]("name") - (2.0) Set member of guild as a new Guilmaster. Only Guildmaster.
: [[API GuildUninviteByName|GuildUninviteByName]]("name") - (2.0) kicks the defined player from the guild. (replaced by [[API GuildUninvite|GuildUninvite]]("name")).
: [[API SaveGuildRoster|SaveGuildRoster]]() - (3.2.2) Removed in favor of the Armory.
: [[API SetGuildBankTabWithdraw|SetGuildBankTabWithdraw]](tab, amount) - (4.0) Modifies the stacks per day withdraw limit for select guild bank tab. Guild Leader Only.
: [[API SetGuildBankWithdrawLimit|SetGuildBankWithdrawLimit]](amount) - (4.0) Sets the gold withdraw limit from the guild bank. Guild Leader Only.  Renamed to [[API SetGuildBankWithdrawGoldLimit|SetGuildBankWithdrawGoldLimit]]

===Looking for Group Functions===
: [[API AcceptLFGMatch|AcceptLFGMatch]]() - (3.3.0)
: [[API CanSendLFGQuery|CanSendLFGQuery]](typeID, lfgNdx) - (3.3.0)
: [[API CancelPendingLFG|CancelPendingLFG]]() - (3.3.0) Takes the player out of all LFG queues.
: [[API ClearLFGAutojoin|ClearLFGAutojoin]]() - (3.3.0) Disables LFG auto join (being invited to other groups automatically).
: [[API ClearLFMAutofill|ClearLFMAutofill]]() - (3.3.0) Disables LFM auto fill (inviting other players automatically). 
: [[API ClearLookingForGroup|ClearLookingForGroup]]() - (3.3.0)
: [[API ClearLookingForMore|ClearLookingForMore]]() - (3.3.0)
: [[API DeclineLFGMatch|DeclineLFGMatch]]() - (3.3.0)
: [[API GetAvailableRoles|GetAvailableRoles]]() - (4.0) Returns which LFG roles your character may fulfill.
: [[API GetLFGPartyResults|GetLFGPartyResults]](type, lfgNdx, index, partyIndex) - (3.3.0)
: [[API GetLFGResults|GetLFGResults]](type, lfgNdx, index) - (3.3.0)
: [[API GetLFGStatusText|GetLFGStatusText]]() - (3.3.0)
: [[API GetLFGTypeEntries|GetLFGTypeEntries]](type) - (3.3.0)
: [[API GetLookingForGroup|GetLookingForGroup]]() - (3.3.0) returns the player's current LFG state.
: [[API GetNumLFGResults|GetNumLFGResults]](type, lfgNdx) - (3.3.0)
: [[API IsInLFGQueue|IsInLFGQueue]]() - (3.3.0)
: [[API LFGQuery|LFGQuery]](typeID, lfgNdx [, class]) - (3.3.0)
: [[API SetLFGAutojoin|SetLFGAutojoin]]() - (3.3.0) Enables LFG auto join (automatic invites to other groups).
: [[API SetLFGType|SetLFGType]](slot, type) - (3.3.0)
: [[API SetLFMAutofill|SetLFMAutofill]]() - (3.3.0) Enables LFM auto fill (sending automatic invites to other players).
: [[API SetLFMType|SetLFMType]]() - (3.3.0)
: [[API SetLookingForGroup|SetLookingForGroup]](slot, type, index) - (3.3.0) sets a looking for group destination for one of the tree LFG slots.
: [[API SetLookingForMore|SetLookingForMore]]() - (3.3.0)
: [[API SortLFG|SortLFG]]("type") - (3.3.0)

===Lottery Functions===
The following funtions were added in 1.12, but never actually used; subsequently removed in 2.3.
: [[API BuyRandomPicks|BuyRandomPicks]](count) - (2.3)
: [[API CloseLottery|CloseLottery]] - (2.3)
: [[API GetJackpotAmount|GetJackpotAmount]] - (2.3)
: [[API GetLastLotteryNumbers|GetLastLotteryNumbers]] - (2.3)
: [[API GetLotteryPrizeInfo|GetLotteryPrizeInfo]] - (2.3)
: [[API GetMoneyPrizes|GetMoneyPrizes]] - (2.3)
: [[API GetNextDrawTime|GetNextDrawTime]] - (2.3)
: [[API GetNumLotteryPrizes|GetNumLotteryPrizes]] - (2.3)
: [[API GetNumPastDrawResults|GetNumPastDrawResults]] - (2.3)
: [[API GetPastDrawResult|GetPastDrawResult]] - (2.3)
: [[API SubmitNumbers|SubmitNumbers]] - (2.3)

===Mail Functions===
: [[API AddSendMailCOD|AddSendMailCOD]]()
: [[API AddSendMailMoney|AddSendMailMoney]]()
: [[API GetNumPackages|GetNumPackages]]() - Not yet fully implemented. Currently it always returns 1.
: [[API GetPackageInfo|GetPackageInfo]](index) - Not yet fully implemented. Currently an index of 1 returns "Test Package".
: [[API GetNumStationeries|GetNumStationeries]]() -(7.0) Not yet fully implemented. Currently it always returns 1.
: [[API GetSelectedStationeryTexture|GetSelectedStationeryTexture]]() - (7.0) Not yet fully implemented. Currently it returns "STATIONERYTEST" when the mailbox is open.
: [[API GetStationeryInfo|GetStationeryInfo]](index) - (7.0) Not yet fully implemented. Currently an index of 1 returns "Default Stationery".
: [[API PickupSendMailCOD|PickupSendMailCOD]](amount) - This does not appear to exist any longer.
: [[API PickupSendMailMoney|PickupSendMailMoney]](amount) - This does not appear to exist any longer.
: [[API SelectPackage|SelectPackage]](index) - Not yet fully implemented. It does nothing visible.
: [[API SelectStationery|SelectStationery]](index) - (7.0) Not yet fully implemented. It does nothing visible.

===Mount Journal Functions===
: {{api|C_MountJournal.GetMountInfoExtra}}(7.0.3) - Returns extra information about the specified mount.
: {{api|C_MountJournal.GetMountInfo}}(7.0.3) - Returns information about the specified mount.
: {{api|C_MountJournal.Summon}}(7.0.3) - Summons the specified mount.

===Map Functions===
: [[API SetupWorldMapScale|SetupWorldMapScale]]() (1.12) replaced by [[API SetupFullscreenScale|SetupFullscreenScale]].

===Party Functions===
: [[API CanSendInvite|CanSendInvite]]() - Returns true or false for if player can invite players to current event
: [[API InviteToParty|InviteToParty]]("unit") - (2.0) Invite a unit to a party by its unit id (likely "target") ''(replaced by [[API InviteUnit|InviteUnit]]("unit"))''
: [[API PromoteByName|PromoteByName]]("name") - Promotes by name the target. (Probably {{api|PromoteToLeader}}).
: [[API UninviteByName|UninviteByName]]("name") - (2.0) Uninvites (kicks) the named player from the current group if player is group leader. (replaced by [[API UninviteUnit| UninviteUnit]]("unit")). 
: [[API UninviteFromParty|UninviteFromParty]]("unit") - (2.0) Kick a unit from the party if player is group leader. (replaced by [[API UninviteUnit|UninviteUnit]]("unit")).

===Pet Functions===
: [[API BuyStableSlot|BuyStableSlot]]() - (4.0)
: [[API ClickStablePet|ClickStablePet]](index) - (4.0) ?.
: [[API GetNextStableSlotCost|GetNextStableSlotCost]]() - (4.0) 
: [[API GetNumStablePets|GetNumStablePets]]() - (4.0) Returns the number of pets in the stable.
: [[API GetNumStableSlots|GetNumStableSlots]]() - (4.0) Returns the number of stable slots you own.
: [[API GetSelectedStablePet|GetSelectedStablePet]]() - (4.0) ?.
: [[API StablePet|StablePet]](index) - (4.0) Puts your pet into the specified stable slot
: [[API UnstablePet|UnstablePet]](index) - (4.0) Retrieves a pet from the specified stable slot

===Pet Journal Functions===
: [[API C_PetJournal.AddAllPetSourcesFilter|C_PetJournal.AddAllPetSourcesFilter]]() - (7.0.3) Enables all pet sources in the filter menu.
: [[API C_PetJournal.AddAllPetTypesFilter|C_PetJournal.AddAllPetTypesFilter]]() - (7.0.3) Enables all pet types in the filter menu.
: [[API C_PetJournal.ClearAllPetSourcesFilter|C_PetJournal.ClearAllPetSourcesFilter]]() - (7.0.3) Clears all pet sources in the filter menu.
: [[API C_PetJournal.ClearAllPetTypesFilter|C_PetJournal.ClearAllPetTypesFilter]]() - (7.0.3) Clears all pet types in the filter menu.
: [[API C_PetJournal.IsFlagFiltered|C_PetJournal.IsFlagFiltered]](flag) - (7.0.3) Returns true if the selected flag is unchecked.
: [[API C_PetJournal.IsPetSourceFiltered|C_PetJournal.IsPetSourceFiltered]](index) - (7.0.3) Returns true if the pet source is unchecked.
: [[API C_PetJournal.IsPetTypeFiltered|C_PetJournal.IsPetTypeFiltered]](index) - (7.0.3) Returns true if the pet type is unchecked.
: [[API C_PetJournal.SetFlagFilter|C_PetJournal.SetFlagFilter]](flag, value) - (7.0.3) Sets the flags in the filter menu.
: [[API C_PetJournal.SetPetSourceFilter|C_PetJournal.SetPetSourceFilter]](index, value) - (7.0.3) Sets the pet source in the filter menu.

===Petition Functions===
: [[API BuyPetition|BuyPetition]](arenaFormat, "teamName") - (4.0) Purchases an arena team charter.
: [[API TurnInArenaPetition|TurnInArenaPetition]](teamSize, ...) - (4.0) Founds an arena team.

===PVP Functions===
: [[API GetHonorCurrency|GetHonorCurrency]]() - (4.0) Return the amount of honor the player has available to purchase items.

===Quest Functions===
: [[API ShiftQuestWatches|ShiftQuestWatches]](id1, id2) - Exchanges the order of two watched quests.

===RealID (BNet) Functions===
: [[API BNCreateConversation|BNCreateConversation]](id,id) - (6.2.4)
: [[API BNGetBlockedToonInfo|BNGetBlockedToonInfo]](index) - (6.2.4)
: [[API BNGetConversationInfo|BNGetConversationInfo]](chatTarget) - (6.2.4) returns unknown
: [[API BNGetConversationMemberInfo|BNGetConversationMemberInfo]](conversationID, memberID) - (6.2.4) returns accountID, toonID, name
: [[API BNGetCustomMessageTable|BNGetCustomMessageTable]](table) - (6.2.4)
: [[API BNGetFriendToonInfo|BNGetFriendToonInfo]](friendIndex, toonIndex) - (6.2.4)
: [[API BNGetMatureLanguageFilter|BNGetMatureLanguageFilter]]() - (6.2.4)
: [[API BNGetMaxPlayersInConversation|BNGetMaxPlayersInConversation]]() - (6.2.4)
: [[API BNGetNumBlockedToons|BNGetNumBlockedToons]]() - (6.2.4)
: [[API BNGetNumConversationMembers|BNGetNumConversationMembers]](conversationID) - (6.2.4)
: [[API BNGetNumFriendToons|BNGetNumFriendToons]](index) - (6.2.4)
: [[API BNGetSelectedToonBlock|BNGetSelectedToonBlock]]() - (6.2.4)
: [[API BNGetToonInfo|BNGetToonInfo]](toonID or presenceID) - (6.2.4) returns hasFocus, toonName, client, realmName, realmID, faction, race, class, guild, zoneName, level, gameText
: [[API BNInviteToConversation|BNInviteToConversation]](target, player) - (6.2.4)
: [[API BNIsToonBlocked|BNIsToonBlocked]](ID) - (6.2.4)
: [[API BNLeaveConversation|BNLeaveConversation]](channel) - (6.2.4)
: [[API BNListConversation|BNListConversation]](channel) - (6.2.4)
: [[API BNReportFriendInvite|BNReportFriendInvite]](ID) - (6.2.4)
: [[API BNSendConversationMessage|BNSendConversationMessage]](channel,text) - (6.2.4)
: [[API BNSetFocus|BNSetFocus]]() - (6.2.4)
: [[API BNSetMatureLanguageFilter|BNSetMatureLanguageFilter]](bool) - (6.2.4)
: [[API BNSetSelectedToonBlock|BNSetSelectedToonBlock]](index) - (6.2.4)
: [[API BNSetToonBlocked|BNSetToonBlocked]](ID, bool) - (6.2.4)
: [[API CanCooperateWithToon|CanCooperateWithToon]](toonID) - (6.2.4)

===Reporting Functions===
: [[API ReportBug|ReportBug("text")]] - (1.3.0)
: [[API ReportNote|ReportNote("text")]] - (1.3.0)
: [[API ReportSuggestion|ReportSuggestion("text","category")]] - (1.3.0)

===Settings Functions===
: [[API DownloadSettings|DownloadSettings]]() - (6.0.2) Download a backup of your settings from the server. - Removed in 6.0.2
: [[API GetBaseMip|GetBaseMip]]() - (4.0) Get the world appearance Texture Detail.
: [[API GetCVarAbsoluteMax|GetCVarAbsoluteMax]]("cVar") - (4.0) Returns the maximum value a cVar will hold
: [[API GetCVarAbsoluteMin|GetCVarAbsoluteMin]]("cVar") - (4.0) Returns the minimum value a cVar will hold
: [[API GetCVarMax|GetCVarMax]]("cVar") - (4.0) Returns the maximum value acceptable for a cVar
: [[API GetCVarMin|GetCVarMin]]("cVar") - (4.0) Returns the minimum value acceptable for a cVar
: [[API GetCurrentMultisampleFormat|GetCurrentMultisampleFormat]]() - (6.0.2) Get the current in-use multi-sample (antialias) format.
: [[API GetFarclip|GetFarclip]]() - (4.0) Get the world appearance Terrain Distance.
: [[API GetMultisampleFormats|GetMultisampleFormats]]() - (6.0.2) Get the available multi-sample (antialias) formats..
: [[API GetTerrainMip|GetTerrainMip]]() - (4.0) Get the world appearance Terrain Texture.
: [[API GetTexLodBias|GetTexLodBias]]() - (4.0) 
: [[API GetWaterDetail|GetWaterDetail]]() - (4.0) 
: [[API ResetPerformanceValues|ResetPerformanceValues]]()
: [[API SetBaseMip|SetBaseMip]](value) - (4.0) Set the world appearance Texture Detail (0,1).
: [[API SetFarclip|SetFarclip]](value) - (4.0) Set the world appearance Terrain Distance.
: [[API SetMultisampleFormat|SetMultisampleFormat]](index) - (6.0.2) Set the multi-sample (antialias) format to use.
: [[API SetTerrainMip|SetTerrainMip]](value) - (4.0) Set the world appearance Terrain Texture (0,1).
: [[API SetTexLodBias|SetTexLodBias]]() - (4.0) 
: [[API SetWaterDetail|SetWaterDetail]]() - (4.0)
: [[API TutorialsEnabled|TutorialsEnabled]]() - (3.3.0) Probably replaced by a cVar
: [[API UploadSettings|UploadSettings]]() - (6.0.2) Uploads a backup of your settings to the server.

===Skill Functions===
: [[API AcceptSkillUps|AcceptSkillUps]]() - (4.0) Accepts changes to skills; unused on live realms.
: [[API AddSkillUp|AddSkillUp]](index) - (4.0) Spends skill points to improve a skill; unused on live realms.
: [[API BuySkillTier|BuySkillTier]](index) - (4.0) Learns the next tier of a skill; unused on live realms.
: [[API CancelSkillUps|CancelSkillUps]]() - (4.0) Rejects changes to skills; unused on live realms.
: [[API CollapseSkillHeader|CollapseSkillHeader]](index) - (4.0) 
: [[API ExpandSkillHeader|ExpandSkillHeader]](index) - (4.0) 
: [[API GetAdjustedSkillPoints|GetAdjustedSkillPoints]]() - (4.0) 
: [[API GetNumSkillLines|GetNumSkillLines]]() - (4.0) get the number of lines in the skill window, including headers
: [[API GetSelectedSkill|GetSelectedSkill]]() - (4.0) 
: [[API GetSkillLineInfo|GetSkillLineInfo]](index) - (4.0) get the information for a selected skill
: [[API RemoveSkillUp|RemoveSkillUp]](index) - (4.0) 
: [[API SetSelectedSkill|SetSelectedSkill]](index) - (4.0) 

===Spell Functions===
: [[API GetKnownSlotFromHighestRankSlot|GetKnownSlotFromHighestRankSlot]](slot) - (4.0) ? Ranks were removed from the game in patch 4.0.
: [[API GetSpellName|GetSpellName]](spellID, "bookType") - (4.0) Returns the spell name and spell rank for a spell in the player's spellbook.  Use [[API GetSpellBookItemName|GetSpellBookItemName]]
: [[API UpdateSpells|UpdateSpells]]() - (4.0) Ensures spells in spellbook are loaded, fires "SPELLS_CHANGED" event when it is done.


===Specialization Functions===
: NOCOMBAT [[API SetActiveSpecGroup|SetActiveSpecGroup]](groupIndex) - Changes the active specialization group.

===System Functions===
: [[API CheckReadyCheckTime|CheckReadyCheckTime]]() - (3.3) Unknown, called from UIParent's OnUpdate!
: [[API GetDoodadAnim|GetDoodadAnim]]() - Retrieved object animation state, possibly for movie scripts.
: [[API GetExistingLocales|GetExistingLocales]]() - (6.0.2) Returns a list of installed language packs.
: [[API GetMovieSubtitles|GetMovieSubtitles]]()
: [[API GetWorldDetail|GetWorldDetail]]() - (3.0.2) Get the world appearance Environment Detail.
: [[API HideFriendNameplates|HideFriendNameplates]]() - Turn off display of nameplates above friendly units. (Now controlled by nameplateShowFriends CVar))
: [[API HideNameplates|HideNameplates]]() - Turn off display of nameplates. (Now controlled by nameplateShowEnemies CVar)
: [[API RestoreVideoEffectsDefaults|RestoreVideoEffectsDefaults]]() - (4.0)
: [[API RestoreVideoResolutionDefaults|RestoreVideoResolutionDefaults]]() - (4.0) 
: [[API RestoreVideoStereoDefaults|RestoreVideoStereoDefaults]]() - (4.0) New in 3.0.8
: [[API SetDoodadAnim|SetDoodadAnim]]() - Controlled object animation state, possibly for movie scripts.
: [[API SetMovieSubtitles|SetMovieSubtitles]](subtitles)
: [[API SetWorldDetail|SetWorldDetail]](value) - (3.0.2) Set the world appearance Environment Detail (0,1,2).
: [[API ShowFriendNameplates|ShowFriendNameplates]]() - Turn on display of nameplates above friendly units. (Now controlled by nameplateShowFriends CVar)
: [[API ShowNameplates|ShowNameplates]]() - Turn on display of nameplates. (Now controlled by nameplateShowEnemies CVar)
: [[API Sound_GetInputDriverNameByIndex|Sound_GetInputDriverNameByIndex]]()
: [[API Sound_GetNumInputDrivers|Sound_GetNumInputDrivers]]()
: [[API Sound_GetNumOutputDrivers|Sound_GetNumOutputDrivers]]()
: [[API Sound_GetOutputDriverNameByIndex|Sound_GetOutputDriverNameByIndex]]()
: [[API Sound_RestartSoundEngine|Sound_RestartSoundEngine]]()
: UI [[API TakeScreenshot|TakeScreenshot]]() - Takes a screenshot.

===Talent Functions===
: [[API GetNumTalents|GetNumTalents]]([inspect]) - (6.0.2) Returns the maximum talent slot index.
: [[API GetTalentClearInfo|GetTalentClearInfo]]() - (7.0.3) Returns information about the current cost of unlearning a talent
: [[API GetTalentRowSelectionInfo|GetTalentRowSelectionInfo]](tier) - (7.0.3) Returns information about the player's talent selection in the specified talent tier.

===Taxi Functions===
: UI [[API DrawRouteLine|DrawRouteLine]](texture, canvas, startx, starty, endx, endy, width, relPoint) - (7.0) Draws a line.
: [[API TaxiNodeSetCurrent|TaxiNodeSetCurrent]](slot) - (7.0) Renumbers slots based on new current slot.

===Toggle Functions===
: UI [[API ToggleCombatLog|ToggleCombatLog]] - (3.3.5) Opens/closes the combat log.
: UI [[API ToggleKeyRing|ToggleKeyRing]] - Opens/closes the key ring.

===Tracking Functions===
: [[API GetTrackingTexture|GetTrackingTexture]]() - (4.0) Return the texture of the current tracking buff, if one is active.

===Trainer Functions===
: [[API CollapseTrainerSkillLine|CollapseTrainerSkillLine]](index) - (4.0) Collapses a header, hiding all spells below it.
: [[API ExpandTrainerSkillLine|ExpandTrainerSkillLine]](index) - (4.0) Expands a header, showing all spells below it.
: [[API GetTrainerServiceStepIncrease|GetTrainerServiceStepIncrease]]() - (4.0) ?.
: [[API GetTrainerServiceStepReq|GetTrainerServiceStepReq]] - (4.0) ?.
: [[API GetTrainerSkillLineFilter|GetTrainerSkillLineFilter]]() - (4.0) ?;
: [[API GetTrainerSkillLines|GetTrainerSkillLines]]() - (4.0) ?;
: [[API IsTrainerServiceLearnSpell|IsTrainerServiceLearnSpell]](index) - Returned whether a trainer was going to teach you a spell.
: [[API IsTrainerServiceSkillStep|IsTrainerServiceSkillStep]]() - (4.0) ?.
: [[API SetTrainerSkillLineFilter|SetTrainerSkillLineFilter]]() - (4.0) ?.

===Transmogrification Functions===
: [[API ApplyTransmogrifications|ApplyTransmogrifications]]() - (7.0.3) Applies all pending transmogrifications, and pays for the cost
: [[API CanTransmogrifyItemWithItem|CanTransmogrifyItemWithItem]](targetItem, sourceItem) - (7.0.3) Returns whether an item can be transmogrified to look like another item.
: [[API ClearTransmogrifySlot|ClearTransmogrifySlot]]([slotId]) - (7.0.3) Clears the specified transmogrify slot
: [[API ClickTransmogrifySlot|ClickTransmogrifySlot]](slotId) - (7.0.3) Facilitates clicking transmogrify slots depending on transmogrify state
: [[API CloseTransmogrifyFrame|CloseTransmogrifyFrame]]() - (7.0.3)
: [[API GetItemTransmogrifyInfo|GetItemTransmogrifyInfo]](itemId) - (7.0.3) Returns how an item can interact with transmogrification.
: [[API GetTransmogrifyCost|GetTransmogrifyCost]]() - (7.0.3) Returns <code>cost, numChanges</code>
: [[API GetTransmogrifySlotInfo|GetTransmogrifySlotInfo]](slotId) - (7.0.3) Returns <code>isTransmogrified, canTransmogrify, cannotTransmogrifyReason, hasPending, hasUndo, visibleItemID, textureName</code>
: [[API UseItemForTransmogrify|UseItemForTransmogrify]](bag, slot, id) - (7.0.3)
: [[API UseVoidItemForTransmogrify|UseVoidItemForTransmogrify]](voidItemslot, inventorySlot) - (7.0.3) Copies the appearance of an item in void storage to an item on your character.
: [[API ValidateTransmogrifications|ValidateTransmogrifications]]() - (7.0.3)

===Unit Functions===
: [[API GetPlayerBuffApplications|GetPlayerBuffApplications]](id or "name"[,"rank"]) - (3.0) Retrieves the number of applications of a debuff or buff. (replaced with [[API UnitBuff|UnitBuff]])
: [[API GetPlayerBuffDispelType|GetPlayerBuffDispelType]](id or "name"[,"rank"]) - (3.0) Get the debuff type for a player debuff ("Magic", "Curse", "Disease", or "Poison".) (replaced with [[API UnitBuff|UnitBuff]])
: [[API IsFeignDeath|IsFeignDeath]]() - (2.1) Returns 1 if the player is feigning death, nil otherwise.  ''See [[API UnitIsFeignDeath|UnitIsFeignDeath]].''
: [[API UnitCharacterPoints|UnitCharacterPoints]]("unit") - (4.0) Returns the number of unspent talent points for the specified unit -- usually 0.
: [[API UnitGetGuildXP|UnitGetGuildXP]]("unit") - (6.0.2) Returns the Guild XP information for a unit. (added in [[Patch 4.0.1]])
: [[API UnitMana|UnitMana]]("unit") - (3.0.2) Returns the current mana (or energy,rage,etc), in points, of the specified unit.
: [[API UnitManaMax|UnitManaMax]]("unit") - (3.0.2) Returns the maximum mana (or energy,rage,etc), in points, of the specified unit.
: [[API UnitIsTapped|UnitIsTapped]]("unit") - (7.0.3) Returns true if the specified unit is tapped, false otherwise.
: [[API UnitIsTappedByPlayer|UnitIsTappedByPlayer]]("unit") - (7.0.3) Returns true if the specified unit is tapped by the player himself, otherwise false.
: [[API UnitIsTappedByAllThreatList|UnitIsTappedByAllThreatList]]("unit") - (7.0.3) Returns whether the specified unit is a community monster, i.e. whether all players engaged in combat with it will receive kill (quest) credit.

===Quest Functions===
: [[API GetQuestLogRewardTalents|GetQuestLogRewardTalents]] - (7.0.3) Returns number of talents awarded for quest completion from quest log.
: [[API GetRewardTalents|GetRewardTalents]]() - (7.0.3) Returns number of talents awarded for quest completion for quest currently in gossip window.
```