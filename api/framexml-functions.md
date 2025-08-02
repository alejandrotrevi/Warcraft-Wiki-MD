# FrameXML functions

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|notitle=1}} {{tocright}}
'''FrameXML functions''' facilitate interacting with the UI.

==UIParent==
: {{i-note|These functions toggle the Interface Panels, but if they use <code>ShowUIPanel()</code> they cannot be called in combat.}}
: {{api|ShowUIPanel}}(<span class="apiarg">frame, force</span>)
: [https://www.townlong-yak.com/framexml/go/PVEFrame_ToggleFrame PVEFrame_ToggleFrame]() - Toggles the Group Finder.
: [https://www.townlong-yak.com/framexml/go/ToggleAchievementFrame ToggleAchievementFrame]() - Shows the Achievements frame.
: [[API ToggleCharacter|ToggleCharacter]](<span class="apiarg">index</span>) - Toggles the character pane to the specified frame.
: [https://www.townlong-yak.com/framexml/go/ToggleCollectionsJournal ToggleCollectionsJournal](<span class="apiarg">index</span>) - Toggles the Collections window.
: [https://www.townlong-yak.com/framexml/go/ToggleEncounterJournal ToggleEncounterJournal]() - Toggles the Adventure Guide.
: [[API ToggleFriendsFrame|ToggleFriendsFrame]](<span class="apiarg">[tabNumber]</span>) - Opens/closes the friends pane, optionally on a specific tab.
: [[API ToggleGameMenu|ToggleGameMenu]]() - Opens/closes the game menu.
: [https://www.townlong-yak.com/framexml/go/ToggleGuildFrame ToggleGuildFrame]() - Toggles the Guild & Communites frame.
: [https://www.townlong-yak.com/framexml/go/ToggleHelpFrame ToggleHelpFrame]() - Opens the Help Request frame.
: [[API ToggleMinimap|ToggleMinimap]]() - Turns the minimap display on/off.
: [[API TogglePVPUI|TogglePVPUI]]() - Opens/closes the PvP frame.
: [[API ToggleSpellBook|ToggleSpellBook]](<span class="apiarg">bookType</span>) - Shows the spellbook. Can show your spells or your pet's.
: [[API ToggleTalentFrame|ToggleTalentFrame]]() - Opens the Talent frame.

: [https://github.com/Gethe/wow-ui-source/search?q=AbbreviateLargeNumbers AbbreviateLargeNumbers](<span class="apiarg">value</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=AbbreviateNumbers AbbreviateNumbers](<span class="apiarg">value</span>)

==Mixins==
: <span class="noexcerpt" data-nosnippet>''See also the [https://github.com/Ketho/BlizzardInterfaceResources/blob/mainline/Resources/Mixins.lua Complete list]'' of mixins</span>
[[Wikipedia:Mixin|Mixin]]s are similar to classes in OOP languages. An object can "inherit" from multiple mixins.
: [https://www.townlong-yak.com/framexml/go/Mixin Mixin](<span class="apiarg">object, ...</span>) - Copies mixins into an existing object.
: [https://www.townlong-yak.com/framexml/go/CreateFromMixins CreateFromMixins](<span class="apiarg">...</span>) - Copies mixins into a new object.

: [https://www.townlong-yak.com/framexml/go/CreateColor CreateColor](<span class="apiarg">r, g, b, a</span>) - Returns a [[ColorMixin]] object.
: [https://www.townlong-yak.com/framexml/go/CreateRectangle CreateRectangle](<span class="apiarg">left, right, top, bottom</span>) - Returns a [[RectangleMixin]] object.
: [https://www.townlong-yak.com/framexml/go/CreateVector2D CreateVector2D](<span class="apiarg">x, y</span>) - Returns a [[Vector2DMixin]] object.
: [https://www.townlong-yak.com/framexml/go/CreateVector3D CreateVector3D](<span class="apiarg">x, y, z</span>) - Returns a [[Vector3DMixin]] object.
: [https://www.townlong-yak.com/framexml/9.0.2/ObjectAPI/Spell.lua#4 SpellMixin:CreateFromSpellID](<span class="apiarg">spellID</span>) - Returns a [[SpellMixin]] object.
: [https://www.townlong-yak.com/framexml/9.0.2/ObjectAPI/Item.lua#40 Item:CreateFromItemID](<span class="apiarg">itemID</span>) - Returns an [[ItemMixin]] object.
: [https://www.townlong-yak.com/framexml/9.0.2/ObjectAPI/ItemLocation.lua#9 ItemLocation:CreateFromBagAndSlot]() - Returns an [[ItemLocationMixin]] object.
: [https://www.townlong-yak.com/framexml/9.0.2/ObjectAPI/PlayerLocation.lua#4 PlayerLocation:CreateFromGUID](<span class="apiarg">guid</span>) - Returns a [[PlayerLocationMixin]] object.
: [https://www.townlong-yak.com/framexml/9.0.2/TransmogUtil.lua#76 TransmogUtil.CreateTransmogLocation](<span class="apiarg">slotDescriptor, transmogType, modification</span>) - Returns a [[TransmogLocationMixin]] object.
: [[CallbackRegistryMixin]]

: [https://www.townlong-yak.com/framexml/go/AnchorMixin AnchorMixin]
: [https://www.townlong-yak.com/framexml/go/AnimatedNumericFontStringMixin AnimatedNumericFontStringMixin]
: [https://www.townlong-yak.com/framexml/go/DoublyLinkedListMixin DoublyLinkedListMixin]
: [https://www.townlong-yak.com/framexml/go/GridLayoutMixin GridLayoutMixin]
: [https://www.townlong-yak.com/framexml/go/LineMixin LineMixin]
: [https://www.townlong-yak.com/framexml/go/MapCanvasMixin MapCanvasMixin]
: [https://www.townlong-yak.com/framexml/go/SecondsFormatterMixin SecondsFormatterMixin]
: [https://www.townlong-yak.com/framexml/go/SparseGridMixin SparseGridMixin]
: [https://www.townlong-yak.com/framexml/go/TextureLoadingGroupMixin TextureLoadingGroupMixin]

: [[API CreateObjectPool|CreateObjectPool]](<span class="apiarg">creationFunc, resetterFunc</span>) - Creates a [[ObjectPoolMixin]] object for [[UIOBJECT UIObject|widgets]].
: [[API CreateFramePool|CreateFramePool]](<span class="apiarg">frameType [, parent, frameTemplate, resetterFunc, forbidden]</span>) - Creates a [[FramePoolMixin]] for [[UIOBJECT Frame|Frames]].
: [[API CreateTexturePool|CreateTexturePool]](<span class="apiarg">parent [, layer, subLayer, textureTemplate, resetterFunc]</span>) - Creates a [[TexturePoolMixin]] for [[UIOBJECT Texture|Textures]].
: [[API CreateFontStringPool|CreateFontStringPool]](<span class="apiarg">parent [, layer, subLayer, fontStringTemplate, resetterFunc]</span>) - Creates a [[FontStringPoolMixin]] for [[UIOBJECT FontString|FontStrings]].
: [[API CreateActorPool|CreateActorPool]](<span class="apiarg">parent [, actorTemplate, resetterFunc]</span>) - Creates an [[ActorPoolMixin]] for [[UIOBJECT Actor|Actors]].
: [https://www.townlong-yak.com/framexml/go/CreateFramePoolCollection CreateFramePoolCollection]() - Creates a [[FramePoolCollectionMixin]] object for [[FramePoolMixin|frame pools]].

==Blizzard_ChatFrameBase==
===ChatFrame===
: [[API ChatFrame_AddChannel|ChatFrame_AddChannel]](<span class="apiarg">chatFrame, channelName</span>) - Activates channel in chatFrame.
: [[API ChatFrame_AddMessageEventFilter|ChatFrame_AddMessageEventFilter]](<span class="apiarg">event, filterFunc</span>) - Adds a chat message filtering function.
: [[API ChatFrame_GetMessageEventFilters|ChatFrame_GetMessageEventFilters]](<span class="apiarg">event</span>) - Retrieves the list of chat message filtering functions.
: [[API ChatFrame_OnHyperlinkShow|ChatFrame_OnHyperlinkShow]](<span class="apiarg">reference, link, button</span>) - Called when the user clicks on a chatlink.
: [[API ChatFrame_RemoveMessageEventFilter|ChatFrame_RemoveMessageEventFilter]](<span class="apiarg">event, filterFunc</span>) - Unregisters a chat message filtering function.

==Blizzard_FrameXML==
===EquipmentManager===
: [[API EquipmentManager_UnpackLocation|EquipmentManager_UnpackLocation]]() - Unpacks a location integer to determine the actual inventory location.

==Blizzard_SharedXMLBase==
===FrameUtil===
: [[API UIFrameFadeIn|UIFrameFadeIn]](<span class="apiarg">frame, timeToFade, startAlpha, endAlpha</span>) - Fades a frame in.
: [[API UIFrameFadeOut|UIFrameFadeOut]](<span class="apiarg">frame, timeToFade, startAlpha, endAlpha</span>) - Fades a frame out.

===TextureUtil===
: [https://www.townlong-yak.com/framexml/go/CreateAtlasMarkup CreateAtlasMarkup](<span class="apiarg">atlasName [, height, width, offsetX, offsetY]</span>) - Returns a texture fontstring for an atlas.
: [https://www.townlong-yak.com/framexml/go/CreateTextureMarkup CreateTextureMarkup](<span class="apiarg">file, fileWidth, fileHeight, width, height, left, right, top, bottom [, xOffset, yOffset]</span>) - Returns a texture fontstring.
: [https://www.townlong-yak.com/framexml/go/GetTextureInfo GetTextureInfo](<span class="apiarg">obj</span>) - Returns the type and info of a texture.

==Blizzard_UIPanels_Game==
===ContainerFrame===
: {{api|CloseAllBags}}(<span class="apiarg">callingFrame, forceUpdate</span>)
: {{api|CloseBackpack}}()
: {{api|CloseBag}}(<span class="apiarg">bagID</span>)
: {{api|IsBagOpen}}(<span class="apiarg">bagID</span>)
: {{api|OpenAllBags}}(<span class="apiarg">callingFrame, forceUpdate</span>)
: {{api|OpenBackpack}}()
: {{api|OpenBag}}(<span class="apiarg">bagID, force</span>)
: {{api|ToggleAllBags}}()
: {{api|ToggleBackpack}}() - Toggles your backpack open/closed.
: {{api|ToggleBag|ToggleBag}}(<span class="apiarg">bagID</span>) - Opens or closes the specified bag.

===DressUpFrames===
The [[Dressing room]] was added in [[Patch 1.7.0]]
: [https://www.townlong-yak.com/framexml/go/DressUpItemLink DressUpItemLink](<span class="apiarg">itemLink</span>) - Shows the Dressing Room with the given item equipped.
: [https://www.townlong-yak.com/framexml/go/DressUpMountLink DressUpMountLink](<span class="apiarg">itemLink | spellLink</span>) - Shows the Dressing Room for the mount.
: [https://www.townlong-yak.com/framexml/go/DressUpTransmogLink DressUpTransmogLink](<span class="apiarg">transmogLink</span>) - Shows the Dressing Room for transmog appearance or illusion.
: [https://www.townlong-yak.com/framexml/go/SetDressUpBackground SetDressUpBackground](<span class="apiarg">frame, fileName, atlasPostfix</span>)

==Blizzard_UIParent==
===UIParent===
: [[API MouseIsOver|MouseIsOver]](<span class="apiarg">region, topOffset, bottomOffset, leftOffset, rightOffset</span>) - Checks whether the mouse is over the frame (or within specified offsets).

==[https://github.com/Gethe/wow-ui-source/tree/live/Interface/SharedXML SharedXML]==
====AccountUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GameLimitedMode_IsActive GameLimitedMode_IsActive]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetClampedCurrentExpansionLevel GetClampedCurrentExpansionLevel]()

====AnchorUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=CreateAnchor AnchorUtil.CreateAnchor](<span class="apiarg">point, relativeTo, relativePoint, x, y</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CreateGridLayout AnchorUtil.CreateGridLayout](<span class="apiarg">direction, rowSize, spacingX, spacingY</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CreateAnchorFromPoint AnchorUtil.CreateAnchorFromPoint](<span class="apiarg">region, pointIndex</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GridLayout AnchorUtil.GridLayout](<span class="apiarg">frames, initialAnchor, layout</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GridLayoutFactoryByCount AnchorUtil.GridLayoutFactoryByCount](<span class="apiarg">factoryFunction, count, initialAnchor, layout</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GridLayoutFactory AnchorUtil.GridLayoutFactory](<span class="apiarg">factoryFunction, initialAnchor, totalWidth, totalHeight, overrideDirection, overridePaddingX, overridePaddingY</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=MirrorRegionsAlongVerticalAxis AnchorUtil.MirrorRegionsAlongVerticalAxis](<span class="apiarg">mirrorDescriptions</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=MirrorRegionsAlongHorizontalAxis AnchorUtil.MirrorRegionsAlongHorizontalAxis](<span class="apiarg">mirrorDescriptions</span>)

====AuraUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=FindAura AuraUtil.FindAura](<span class="apiarg">predicate, unit, filter, predicateArg1, predicateArg2, predicateArg3</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FindAuraByName AuraUtil.FindAuraByName](<span class="apiarg">auraName, unit, filter</span>) - Finds the first aura that matches the name.
: [https://github.com/Gethe/wow-ui-source/search?q=ForEachAura AuraUtil.ForEachAura](<span class="apiarg">unit, filter, maxCount, func</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ShouldSkipAuraUpdate AuraUtil.ShouldSkipAuraUpdate](<span class="apiarg">isFullUpdate, updatedAuraInfos, isRelevantFunc, ...</span>)

====ColorUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=CreateColorFromHexString CreateColorFromHexString](<span class="apiarg">hexColor</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CreateColorFromBytes CreateColorFromBytes](<span class="apiarg">r, g, b, a</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=AreColorsEqual AreColorsEqual](<span class="apiarg">left, right</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetClassColor GetClassColor](<span class="apiarg">classFilename</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetClassColorObj GetClassColorObj](<span class="apiarg">classFilename</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetClassColoredTextForUnit GetClassColoredTextForUnit](<span class="apiarg">unit, text</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetFactionColor GetFactionColor](<span class="apiarg">factionGroupTag</span>)

====CvarUtil====
: [http://townlong-yak.com/framexml/go/RegisterCVar RegisterCVar](<span class="apiarg">name, value</span>)
: [http://townlong-yak.com/framexml/go/ResetTestCvars ResetTestCvars]()
: [http://townlong-yak.com/framexml/go/SetCVar SetCVar](<span class="apiarg">name, value, eventName</span>) : <span class="apiret">success</span>
: [http://townlong-yak.com/framexml/go/GetCVar GetCVar](<span class="apiarg">name</span>) : <span class="apiret">value</span>
: [http://townlong-yak.com/framexml/go/SetCVarBitfield SetCVarBitfield](<span class="apiarg">name, index, value, scriptCVar</span>) : <span class="apiret">success</span>
: [http://townlong-yak.com/framexml/go/SetCVarToDefault SetCVarToDefault](<span class="apiarg">name</span>) - Resets a CVar to default.
: [http://townlong-yak.com/framexml/go/GetCVarBitfield GetCVarBitfield](<span class="apiarg">name, index</span>) : <span class="apiret">''boolean''</span>
: [http://townlong-yak.com/framexml/go/GetCVarBool GetCVarBool](<span class="apiarg">name</span>) : <span class="apiret">''boolean''</span>
: [http://townlong-yak.com/framexml/go/GetCVarDefault GetCVarDefault](<span class="apiarg">name</span>) : <span class="apiret">value</span>

====EasingUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=InQuadratic EasingUtil.InQuadratic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=OutQuadratic EasingUtil.OutQuadratic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=InOutQuadratic EasingUtil.InOutQuadratic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=InCubic EasingUtil.InCubic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=OutCubic EasingUtil.OutCubic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=InOutCubic EasingUtil.InOutCubic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=InQuartic EasingUtil.InQuartic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=OutQuartic EasingUtil.OutQuartic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=InOutQuartic EasingUtil.InOutQuartic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=InQuintic EasingUtil.InQuintic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=OutQuintic EasingUtil.OutQuintic](<span class="apiarg">percent</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=InOutQuintic EasingUtil.InOutQuintic](<span class="apiarg">percent</span>)

====ErrorUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=CallErrorHandler CallErrorHandler](<span class="apiarg">...</span>)

====[[EventRegistry]]====
: <code>CallbackRegistryMixin:RegisterCallback</code>(<span style="font-size:smaller; color:#ecbc2a">event, func, ...</span>)
: <code>CallbackRegistryMixin:TriggerEvent</code>(<span style="font-size:smaller; color:#ecbc2a">event, ...</span>)
: <code>EventRegistry:RegisterFrameEventAndCallback</code>(<span style="font-size:smaller; color:#ecbc2a">event, func, ...</span>)

====EventUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=ContinueAfterAllEvents EventUtil.ContinueAfterAllEvents](callback, ...)
: [https://github.com/Gethe/wow-ui-source/search?q=ContinueOnVariablesLoaded EventUtil.ContinueOnVariablesLoaded](callback)
: [https://github.com/Gethe/wow-ui-source/search?q=ContinueOnAddOnLoaded EventUtil.ContinueOnAddOnLoaded](addOnName, callback)
: [https://github.com/Gethe/wow-ui-source/search?q=RegisterOnceFrameEventAndCallback EventUtil.RegisterOnceFrameEventAndCallback](frameEvent, callback, ...)
: [https://github.com/Gethe/wow-ui-source/search?q=CreateCallbackHandleContainer EventUtil.CreateCallbackHandleContainer]()

====Flags====
: [https://github.com/Gethe/wow-ui-source/search?q=Flags_CreateMask Flags_CreateMask](<span class="apiarg">...</span>) - Creates a bitmask.
: [https://github.com/Gethe/wow-ui-source/search?q=Flags_CreateMaskFromTable Flags_CreateMaskFromTable](<span class="apiarg">flagsTable</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsSet FlagsUtil.IsSet](<span class="apiarg">bitMask, flagOrMask</span>)

====FormattingUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=SplitTextIntoLines SplitTextIntoLines](<span class="apiarg">text, delimiter</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SplitTextIntoHeaderAndNonHeader SplitTextIntoHeaderAndNonHeader](<span class="apiarg">text</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FormatValueWithSign FormatValueWithSign](<span class="apiarg">value</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FormatLargeNumber FormatLargeNumber](<span class="apiarg">amount</span>) - Formats a number with dot or comma number seperators.
: [https://github.com/Gethe/wow-ui-source/search?q=GetMoneyString GetMoneyString](<span class="apiarg">money, separateThousands</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FormatPercentage FormatPercentage](<span class="apiarg">percentage, roundToNearestInteger</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FormatFraction FormatFraction](<span class="apiarg">numerator, denominator</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetHighlightedNumberDifferenceString GetHighlightedNumberDifferenceString](<span class="apiarg">baseString, newString</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FormatUnreadMailTooltip FormatUnreadMailTooltip](<span class="apiarg">tooltip, headerText, senders</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetCurrencyString GetCurrencyString](<span class="apiarg">currencyID, overrideAmount, colorCode, abbreviate</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetCurrenciesString GetCurrenciesString](<span class="apiarg">currencies</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ReplaceGenderTokens ReplaceGenderTokens](<span class="apiarg">string, gender</span>)

====FrameUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=RegisterFrameForEvents FrameUtil.RegisterFrameForEvents](<span class="apiarg">frame, events</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=UnregisterFrameForEvents FrameUtil.UnregisterFrameForEvents](<span class="apiarg">frame, events</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=RegisterFrameForUnitEvents FrameUtil.RegisterFrameForUnitEvents](<span class="apiarg">frame, events, ...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=DoesAncestryInclude DoesAncestryInclude](<span class="apiarg">ancestry, frame</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetUnscaledFrameRect GetUnscaledFrameRect](<span class="apiarg">frame, scale</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyDefaultScale ApplyDefaultScale](<span class="apiarg">frame, minScale, maxScale</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=UpdateScaleForFit UpdateScaleForFit](<span class="apiarg">frame</span>)

====FunctionUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=ExecuteFrameScript ExecuteFrameScript](<span class="apiarg">frame, scriptName, ...</span>) - Manually calls the handler for a frame script.
: [https://github.com/Gethe/wow-ui-source/search?q=CallMethodOnNearestAncestor CallMethodOnNearestAncestor](<span class="apiarg">self, methodName, ...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetValueOrCallFunction GetValueOrCallFunction](<span class="apiarg">tbl, key, ...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GenerateClosure GenerateClosure](<span class="apiarg">f, ...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=RunNextFrame RunNextFrame](<span class="apiarg">callback</span>)

====GameTooltipTemplate====
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddBlankLineToTooltip GameTooltip_AddBlankLineToTooltip](<span class="apiarg">tooltip</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddBodyLine GameTooltip_AddBodyLine](<span class="apiarg">...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddColoredLine GameTooltip_AddColoredLine](<span class="apiarg">tooltip, text, wrap, leftOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddColoredDoubleLine GameTooltip_AddColoredDoubleLine](<span class="apiarg">tooltip, leftText, rightText, leftColor, rightColor, wrap, leftOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddDisabledLine GameTooltip_AddDisabledLine](<span class="apiarg">tooltip, text, wrap, leftOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddErrorLine GameTooltip_AddErrorLine](<span class="apiarg">tooltip, text, wrap, leftOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddHighlightLine GameTooltip_AddHighlightLine](<span class="apiarg">tooltip, text, wrap, leftOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddInstructionLine GameTooltip_AddInstructionLine](<span class="apiarg">tooltip, text, wrap, leftOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddNewbieTip GameTooltip_AddNewbieTip](<span class="apiarg">frame, normalText, r, g, b, newbieText, noNormalText</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_AddNormalLine GameTooltip_AddNormalLine](<span class="apiarg">tooltip, text, wrap, leftOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_InsertFrame GameTooltip_InsertFrame](<span class="apiarg">tooltipFrame, frame, verticalPadding</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_SetTitle GameTooltip_SetTitle](<span class="apiarg">tooltip, text, overrideColor, wrap</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_ShowDisabledTooltip GameTooltip_ShowDisabledTooltip](<span class="apiarg">tooltip, owner, text, tooltipAnchor</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GameTooltip_ShowSimpleTooltip GameTooltip_ShowDisabledTooltip](<span class="apiarg">tooltip, text, overrideColor, wrap, owner, point, offsetX, offsetY</span>)

====InterfaceUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=ReloadUI ReloadUI]()
: [https://github.com/Gethe/wow-ui-source/search?q=OpenToSubscriptionProduct StoreInterfaceUtil.OpenToSubscriptionProduct]()

====LinkUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=ExtractHyperlinkString ExtractHyperlinkString](<span class="apiarg">linkString</span>) - Gets the contents from a [[Hyperlinks|hyperlink]].
: [https://github.com/Gethe/wow-ui-source/search?q=ExtractQuestRewardID ExtractQuestRewardID](<span class="apiarg">linkString</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetItemInfoFromHyperlink GetItemInfoFromHyperlink](<span class="apiarg">link</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetAchievementInfoFromHyperlink GetAchievementInfoFromHyperlink](<span class="apiarg">link</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetURLIndexAndLoadURL GetURLIndexAndLoadURL](<span class="apiarg">self, link</span>)

====MathUtil====
: [http://townlong-yak.com/framexml/go/Lerp Lerp](<span class="apiarg">startValue, endValue, amount</span>) : <span class="apiret">''number''</span> - Linearly interpolates between two values for a parameter <code>amount</code> in the closed unit interval [0, 1]
: [http://townlong-yak.com/framexml/go/Clamp Clamp](<span class="apiarg">value, min, max</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/Saturate Saturate](<span class="apiarg">value</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/Wrap Wrap](<span class="apiarg">value, max</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/ClampDegrees ClampDegrees](<span class="apiarg">value</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/ClampMod ClampMod](<span class="apiarg">value, mod</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/NegateIf NegateIf](<span class="apiarg">value, condition</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/PercentageBetween PercentageBetween](<span class="apiarg">value, startValue, endValue</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/ClampedPercentageBetween ClampedPercentageBetween](<span class="apiarg">value, startValue, endValue</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/DeltaLerp DeltaLerp](<span class="apiarg">startValue, endValue, amount, timeSec</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/FrameDeltaLerp FrameDeltaLerp](<span class="apiarg">startValue, endValue, amount</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/RandomFloatInRange RandomFloatInRange](<span class="apiarg">minValue, maxValue</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/Round Round](<span class="apiarg">value</span>) : <span class="apiret">''number''</span> - Rounds a value.
: [http://townlong-yak.com/framexml/go/Square Square](<span class="apiarg">value</span>) : <span class="apiret">''number''</span> - Squares a value.
: [http://townlong-yak.com/framexml/go/CalculateDistanceSq CalculateDistanceSq](<span class="apiarg">x1, y1, x2, y2</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/CalculateDistance CalculateDistance](<span class="apiarg">x1, y1, x2, y2</span>) : <span class="apiret">''number''</span>
: [http://townlong-yak.com/framexml/go/CalculateAngleBetween CalculateAngleBetween](<span class="apiarg">x1, y1, x2, y2</span>) : <span class="apiret">''number''</span>

====NineSlice====
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyUniqueCornersLayout NineSliceUtil.ApplyUniqueCornersLayout](<span class="apiarg">self, textureKit</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyIdenticalCornersLayout NineSliceUtil.ApplyIdenticalCornersLayout](<span class="apiarg">self, textureKit</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyLayout NineSliceUtil.ApplyLayout](<span class="apiarg">container, userLayout, textureKit</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=DisableSharpening NineSliceUtil.DisableSharpening](<span class="apiarg">container</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyLayoutByName NineSliceUtil.ApplyLayoutByName](<span class="apiarg">container, userLayoutName, textureKit</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetLayout NineSliceUtil.GetLayout](<span class="apiarg">layoutName</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=AddLayout NineSliceUtil.AddLayout](<span class="apiarg">layoutName, layout</span>)

====PixelUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetPixelToUIUnitFactor PixelUtil.GetPixelToUIUnitFactor]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetNearestPixelSize PixelUtil.GetNearestPixelSize](<span class="apiarg">uiUnitSize, layoutScale, minPixels</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetWidth PixelUtil.SetWidth](<span class="apiarg">region, width, minPixels</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetHeight PixelUtil.SetHeight](<span class="apiarg">region, height, minPixels</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetSize PixelUtil.SetSize](<span class="apiarg">region, width, height, minWidthPixels, minHeightPixels</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetPoint PixelUtil.SetPoint](<span class="apiarg">region, point, relativeTo, relativePoint, offsetX, offsetY, minOffsetXPixels, minOffsetYPixels</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetStatusBarValue PixelUtil.SetStatusBarValue](<span class="apiarg">statusBar, value</span>)

====RegionUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=IsDescendantOf RegionUtil.IsDescendantOf](<span class="apiarg">potentialDescendant, potentialAncestor</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsDescendantOfOrSame RegionUtil.IsDescendantOfOrSame](<span class="apiarg">potentialDescendant, potentialAncestorOrSame</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CalculateDistanceSqBetween RegionUtil.CalculateDistanceSqBetween](<span class="apiarg">region1, region2</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CalculateDistanceBetween RegionUtil.CalculateDistanceBetween](<span class="apiarg">region1, region2</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CalculateAngleBetween RegionUtil.CalculateAngleBetween](<span class="apiarg">region1, region2</span>)

====RestrictedInfrastructure====
: [https://github.com/Gethe/wow-ui-source/search?q=tostringall tostringall](<span class="apiarg">...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsFrameHandle IsFrameHandle](<span class="apiarg">handle, protected</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetFrameHandleFrame GetFrameHandleFrame](<span class="apiarg">handle, protected, onlyProtected</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetFrameHandle GetFrameHandle](<span class="apiarg">frame, protected</span>)

====ScriptAnimationUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetScriptAnimationLock ScriptAnimationUtil.GetScriptAnimationLock](<span class="apiarg">region</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ReleaseScriptAnimationLock ScriptAnimationUtil.ReleaseScriptAnimationLock](<span class="apiarg">region</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsScriptAnimationLockActive ScriptAnimationUtil.IsScriptAnimationLockActive](<span class="apiarg">region</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ShakeFrameRandom ScriptAnimationUtil.ShakeFrameRandom](<span class="apiarg">region, magnitude, duration, frequency</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ShakeFrame ScriptAnimationUtil.ShakeFrame](<span class="apiarg">region, shake, maximumDuration, frequency</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GenerateEasedVariationCallback ScriptAnimationUtil.GenerateEasedVariationCallback](<span class="apiarg">easingFunction, distanceX, distanceY, alpha, scale</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=StartScriptAnimation ScriptAnimationUtil.StartScriptAnimation](<span class="apiarg">region, variationCallback, duration, onFinish</span>)

====ScriptedAnimationEffects====
: [https://github.com/Gethe/wow-ui-source/search?q=GetEffectByID ScriptedAnimationEffectsUtil.GetEffectByID](<span class="apiarg">effectID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ReloadDB ScriptedAnimationEffectsUtil.ReloadDB]()

====TableUtil====
: [http://townlong-yak.com/framexml/go/ripairs ripairs](<span class="apiarg">tbl</span>) : <span class="apiret">iter, invariant, init</span> - Reverse iterates over a sequential table.
: [http://townlong-yak.com/framexml/go/tDeleteItem tDeleteItem](<span class="apiarg">tbl, item</span>) - Removes a value from a sequential table.
: [http://townlong-yak.com/framexml/go/tIndexOf tIndexOf](<span class="apiarg">tbl, item</span>) : <span class="apiret">index</span> - Returns the index for a value in a table.
: [http://townlong-yak.com/framexml/go/tContains tContains](<span class="apiarg">tbl, item</span>) : <span class="apiret">''boolean''</span> - Returns true if a sequential table contains a value.
: [http://townlong-yak.com/framexml/go/tCompare tCompare](<span class="apiarg">lhsTable, rhsTable [, depth]</span>) : <span class="apiret">''boolean''</span> - Does a deep compare on the values of the table.
: [http://townlong-yak.com/framexml/go/tInvert tInvert](<span class="apiarg">tbl</span>) : <span class="apiret">''table''</span> - Returns an inverted table.
: [http://townlong-yak.com/framexml/go/tFilter tFilter](<span class="apiarg">tbl, pred, isIndexTable</span>) : <span class="apiret">''table''</span>
: [http://townlong-yak.com/framexml/go/tAppendAll tAppendAll](<span class="apiarg">table, addedArray</span>) - Appends the contents of a sequential table to another table.
: [http://townlong-yak.com/framexml/go/tUnorderedRemove tUnorderedRemove](<span class="apiarg">tbl, index</span>)
: [http://townlong-yak.com/framexml/go/CopyTable CopyTable](<span class="apiarg">settings [, shallow]</span>) : <span class="apiret">''table''</span> - Returns a copy of a table, defaulting to a deep copy.
: [http://townlong-yak.com/framexml/go/AccumulateIf AccumulateIf](<span class="apiarg">tbl, pred</span>) : <span class="apiret">count</span>
: [http://townlong-yak.com/framexml/go/ContainsIf ContainsIf](<span class="apiarg">tbl, pred</span>) : <span class="apiret">''boolean''</span>
: [http://townlong-yak.com/framexml/go/FindInTableIf FindInTableIf](<span class="apiarg">tbl, pred</span>) : <span class="apiret">key, value</span>
: [http://townlong-yak.com/framexml/go/SafePack SafePack](<span class="apiarg">...</span>) : <span class="apiret">''table''</span>
: [http://townlong-yak.com/framexml/go/SafeUnpack SafeUnpack](<span class="apiarg">tbl</span>) : <span class="apiret">...</span>

====TextureUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetTextureInfo GetTextureInfo](<span class="apiarg">obj</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetClampedTextureRotation SetClampedTextureRotation](<span class="apiarg">texture, rotationDegrees</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ClearClampedTextureRotation ClearClampedTextureRotation](<span class="apiarg">texture</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetTexCoordsByGrid GetTexCoordsByGrid](<span class="apiarg">xOffset, yOffset, textureWidth, textureHeight, gridWidth, gridHeight</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetTexCoordsForRole GetTexCoordsForRole](<span class="apiarg">role</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CreateTextureMarkup CreateTextureMarkup](<span class="apiarg">file, fileWidth, fileHeight, width, height, left, right, top, bottom, xOffset, yOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CreateSimpleTextureMarkup CreateSimpleTextureMarkup](<span class="apiarg">file, width, height, xOffset, yOffset</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CreateAtlasMarkup CreateAtlasMarkup](<span class="apiarg">atlasName, width, height, offsetX, offsetY</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetupAtlasesOnRegions SetupAtlasesOnRegions](<span class="apiarg">frame, regionsToAtlases, useAtlasSize</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetFinalNameFromTextureKit GetFinalNameFromTextureKit](<span class="apiarg">fmt, textureKits</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetupTextureKitOnFrame SetupTextureKitOnFrame](<span class="apiarg">textureKit, frame, fmt, setVisibility, useAtlasSize</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetupTextureKitOnFrames SetupTextureKitOnFrames](<span class="apiarg">textureKit, frames, setVisibilityOfRegions, useAtlasSize</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetupTextureKitOnRegions SetupTextureKitOnRegions](<span class="apiarg">textureKit, frame, regions, setVisibilityOfRegions, useAtlasSize</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetupTextureKitsFromRegionInfo SetupTextureKitsFromRegionInfo](<span class="apiarg">textureKit, frame, regionInfoList</span>)

====TimeUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=SecondsToMinutes SecondsToMinutes](<span class="apiarg">seconds</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=MinutesToSeconds MinutesToSeconds](<span class="apiarg">minutes</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=HasTimePassed HasTimePassed](<span class="apiarg">testTime, amountOfTime</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SecondsToClock SecondsToClock](<span class="apiarg">seconds, displayZeroHours</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SecondsToTime SecondsToTime](<span class="apiarg">seconds, noSeconds, notAbbreviated, maxCount, roundUp</span>) - Converts a number of seconds into a readable formatted string.
: [https://github.com/Gethe/wow-ui-source/search?q=SecondsToTimeAbbrev SecondsToTimeAbbrev](<span class="apiarg">seconds</span>) - Converts a number of seconds into a readable and abbreviated formatted string.
: [https://github.com/Gethe/wow-ui-source/search?q=FormatShortDate FormatShortDate](<span class="apiarg">day, month, year</span>)

====UnitUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetPlayerGuid GetPlayerGuid]()
: [https://github.com/Gethe/wow-ui-source/search?q=IsPlayerGuid IsPlayerGuid](<span class="apiarg">guid</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsPlayerInitialSpec IsPlayerInitialSpec]()

==[https://github.com/Gethe/wow-ui-source/tree/live/Interface/FrameXML FrameXML]==

====AchievementUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=IsCriteriaAchievementEarned AchievementUtil.IsCriteriaAchievementEarned](<span class="apiarg">achievementID, criteriaIndex</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsCriteriaReputationGained AchievementUtil.IsCriteriaReputationGained](<span class="apiarg">achievementID, criteriaIndex, checkCriteriaAchievement, countHiddenCriteria</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsCategoryFeatOfStrength AchievementUtil.IsCategoryFeatOfStrength](<span class="apiarg">category</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsFeatOfStrength AchievementUtil.IsFeatOfStrength](<span class="apiarg">achievementID</span>)

====ActionButtonUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=ShowAllActionButtonGrids ActionButtonUtil.ShowAllActionButtonGrids]()
: [https://github.com/Gethe/wow-ui-source/search?q=HideAllActionButtonGrids ActionButtonUtil.HideAllActionButtonGrids]()
: [https://github.com/Gethe/wow-ui-source/search?q=SetAllQuickKeybindButtonHighlights ActionButtonUtil.SetAllQuickKeybindButtonHighlights](<span class="apiarg">show</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ShowAllQuickKeybindButtonHighlights ActionButtonUtil.ShowAllQuickKeybindButtonHighlights]()
: [https://github.com/Gethe/wow-ui-source/search?q=HideAllQuickKeybindButtonHighlights ActionButtonUtil.HideAllQuickKeybindButtonHighlights]()

====AzeriteEssenceUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=HasAnyUnlockableMilestones AzeriteEssenceUtil.HasAnyUnlockableMilestones]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetMilestoneAtPowerLevel AzeriteEssenceUtil.GetMilestoneAtPowerLevel](<span class="apiarg">powerLevel</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetMilestoneSpellInfo AzeriteEssenceUtil.GetMilestoneSpellInfo](<span class="apiarg">milestoneID</span>)

====AzeriteUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=EnumerateEquipedAzeriteEmpoweredItems AzeriteUtil.EnumerateEquipedAzeriteEmpoweredItems]()
: [https://github.com/Gethe/wow-ui-source/search?q=AreAnyAzeriteEmpoweredItemsEquipped AzeriteUtil.AreAnyAzeriteEmpoweredItemsEquipped]()
: [https://github.com/Gethe/wow-ui-source/search?q=DoEquippedItemsHaveUnselectedPowers AzeriteUtil.DoEquippedItemsHaveUnselectedPowers]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetEquippedItemsUnselectedPowersCount AzeriteUtil.GetEquippedItemsUnselectedPowersCount]()
: [https://github.com/Gethe/wow-ui-source/search?q=GenerateRequiredSpecTooltipLine AzeriteUtil.GenerateRequiredSpecTooltipLine](<span class="apiarg">powerID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FindAzeritePowerTier AzeriteUtil.FindAzeritePowerTier](<span class="apiarg">azeriteEmpoweredItemSource, powerID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetSelectedAzeritePowerInTier AzeriteUtil.GetSelectedAzeritePowerInTier](<span class="apiarg">azeriteEmpoweredItemSource, tierIndex</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=HasSelectedAnyAzeritePower AzeriteUtil.HasSelectedAnyAzeritePower](<span class="apiarg">azeriteEmpoweredItemSource</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=DoesBagContainAnyAzeriteEmpoweredItems AzeriteUtil.DoesBagContainAnyAzeriteEmpoweredItems](<span class="apiarg">bagID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsAzeriteItemLocationBankBag AzeriteUtil.IsAzeriteItemLocationBankBag](<span class="apiarg">azeriteItemLocation</span>)

====CalendarUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetCalendarInviteStatusInfo CalendarUtil.GetCalendarInviteStatusInfo](<span class="apiarg">inviteStatus</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetEventBroadcastText CalendarUtil.GetEventBroadcastText](<span class="apiarg">event</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetOngoingEventBroadcastText CalendarUtil.GetOngoingEventBroadcastText](<span class="apiarg">event</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FormatCalendarTimeWeekday CalendarUtil.FormatCalendarTimeWeekday](<span class="apiarg">messageDate</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=AreDatesEqual CalendarUtil.AreDatesEqual](<span class="apiarg">firstCalendarTime, secondCalendarTime</span>)

====CampaignUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=BuildChapterProgressText CampaignUtil.BuildChapterProgressText](<span class="apiarg">campaign, formatString</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetSingleChapterText CampaignUtil.GetSingleChapterText](<span class="apiarg">chapterID, lineSpacing</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=BuildAllChaptersText CampaignUtil.BuildAllChaptersText](<span class="apiarg">campaign, lineSpacing</span>)

====CommunitiesUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetMemberRGB CommunitiesUtil.GetMemberRGB](<span class="apiarg">memberInfo</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SortClubs CommunitiesUtil.SortClubs](<span class="apiarg">clubs</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SortStreams CommunitiesUtil.SortStreams](<span class="apiarg">streams</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SortMemberInfo CommunitiesUtil.SortMemberInfo](<span class="apiarg">clubId, memberInfoArray</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetMemberIdsSortedByName CommunitiesUtil.GetMemberIdsSortedByName](<span class="apiarg">clubId, streamId</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetMemberInfo CommunitiesUtil.GetMemberInfo](<span class="apiarg">clubId, memberIds</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetMemberInfoLookup CommunitiesUtil.GetMemberInfoLookup](<span class="apiarg">memberInfoArray</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetOnlineMembers CommunitiesUtil.GetOnlineMembers](<span class="apiarg">memberInfoArray</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SortMembersByList CommunitiesUtil.SortMembersByList](<span class="apiarg">memberInfoLookup, memberIds</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetAndSortMemberInfo CommunitiesUtil.GetAndSortMemberInfo](<span class="apiarg">clubId, streamId, filterOffline</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=DoesAnyCommunityHaveUnreadMessages CommunitiesUtil.DoesAnyCommunityHaveUnreadMessages]()
: [https://github.com/Gethe/wow-ui-source/search?q=DoesOtherCommunityHaveUnreadMessages CommunitiesUtil.DoesOtherCommunityHaveUnreadMessages](<span class="apiarg">ignoreClubId</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=DoesCommunityHaveUnreadMessages CommunitiesUtil.DoesCommunityHaveUnreadMessages](<span class="apiarg">clubId</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=DoesCommunityHaveOtherUnreadMessages CommunitiesUtil.DoesCommunityHaveOtherUnreadMessages](<span class="apiarg">clubId, ignoreStreamId</span>)	
: [https://github.com/Gethe/wow-ui-source/search?q=GetStreamNotificationSettingsLookup CommunitiesUtil.GetStreamNotificationSettingsLookup](<span class="apiarg">clubId</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=DoesCommunityStreamHaveUnreadMessages CommunitiesUtil.DoesCommunityStreamHaveUnreadMessages](<span class="apiarg">clubId, streamId</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CanKickClubMember CommunitiesUtil.CanKickClubMember](<span class="apiarg">clubPrivileges, memberInfo</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ClearAllUnreadNotifications CommunitiesUtil.ClearAllUnreadNotifications](<span class="apiarg">clubId</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=OpenInviteDialog CommunitiesUtil.OpenInviteDialog](<span class="apiarg">clubId, streamId</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FindCommunityAndStreamByName CommunitiesUtil.FindCommunityAndStreamByName](<span class="apiarg">communityName, streamName</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FindGuildStreamByType CommunitiesUtil.FindGuildStreamByType](<span class="apiarg">clubStreamType</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetRoleSpecClassLine CommunitiesUtil.GetRoleSpecClassLine](<span class="apiarg">classID, specID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=AddLookingForLines CommunitiesUtil.AddLookingForLines](<span class="apiarg">tooltip, recruitingSpecIds, recruitingSpecIdMap, playerSpecs</span>)

====CovenantUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetRenownRewardDisplayData CovenantUtil.GetRenownRewardDisplayData](<span class="apiarg">rewardInfo, onItemUpdateCallback</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetUnformattedRenownRewardInfo CovenantUtil.GetUnformattedRenownRewardInfo](<span class="apiarg">rewardInfo, onItemUpdateCallback</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetRenownRewardInfo CovenantUtil.GetRenownRewardInfo](<span class="apiarg">rewardInfo, onItemUpdateCallback</span>)

====CurrencyContainer====
: [https://github.com/Gethe/wow-ui-source/search?q=GetCurrencyContainerInfo CurrencyContainerUtil.GetCurrencyContainerInfo](<span class="apiarg">currencyID, numItems, name, texture, quality</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetCurrencyContainerInfoForAlert CurrencyContainerUtil.GetCurrencyContainerInfoForAlert](<span class="apiarg">currencyID, quantity, name, texture, quality</span>)

====DifficultyUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetDifficultyName DifficultyUtil.GetDifficultyName](<span class="apiarg">difficultyID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsPrimaryRaid DifficultyUtil.IsPrimaryRaid](<span class="apiarg">difficultyID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetNextPrimaryRaidDifficultyID DifficultyUtil.GetNextPrimaryRaidDifficultyID](<span class="apiarg">difficultyID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetMaxPlayers DifficultyUtil.GetMaxPlayers](<span class="apiarg">difficultyID</span>)

====ItemRef====
: [https://github.com/Gethe/wow-ui-source/search?q=SetItemRef SetItemRef](<span class="apiarg">link, text, button, chatFrame</span>) - Handles item link tooltips in chat.
: [https://github.com/Gethe/wow-ui-source/search?q=GetFixedLink GetFixedLink](<span class="apiarg">text, quality</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetBattlePetAbilityHyperlink GetBattlePetAbilityHyperlink](<span class="apiarg">abilityID, maxHealth, power, speed</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetPlayerLink GetPlayerLink](<span class="apiarg">characterName, linkDisplayText, lineID, chatType, chatTarget</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetBNPlayerLink GetBNPlayerLink](<span class="apiarg">name, linkDisplayText, bnetIDAccount, lineID, chatType, chatTarget</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetGMLink GetGMLink](<span class="apiarg">gmName, linkDisplayText, lineID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetBNPlayerCommunityLink GetBNPlayerCommunityLink](<span class="apiarg">playerName, linkDisplayText, bnetIDAccount, clubId, streamId, epoch, position</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetPlayerCommunityLink GetPlayerCommunityLink](<span class="apiarg">playerName, linkDisplayText, clubId, streamId, epoch, position</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetClubTicketLink GetClubTicketLink](<span class="apiarg">ticketId, clubName, clubType</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetClubFinderLink GetClubFinderLink](<span class="apiarg">clubFinderId, clubName</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetCalendarEventLink GetCalendarEventLink](<span class="apiarg">monthOffset, monthDay, index</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetCommunityLink GetCommunityLink](<span class="apiarg">clubId</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SplitLink LinkUtil.SplitLink](<span class="apiarg">link</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ExtractLink LinkUtil.ExtractLink](<span class="apiarg">text</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsLinkType LinkUtil.IsLinkType](<span class="apiarg">link, matchLinkType</span>)

====ItemUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=RegisterCallback ItemButtonUtil.RegisterCallback](<span class="apiarg">...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=UnregisterCallback ItemButtonUtil.UnregisterCallback](<span class="apiarg">...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=TriggerEvent ItemButtonUtil.TriggerEvent](<span class="apiarg">...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetItemContext ItemButtonUtil.GetItemContext]()
: [https://github.com/Gethe/wow-ui-source/search?q=HasItemContext ItemButtonUtil.HasItemContext]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetItemContextMatchResultForItem ItemButtonUtil.GetItemContextMatchResultForItem](<span class="apiarg">itemLocation</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetItemContextMatchResultForContainer ItemButtonUtil.GetItemContextMatchResultForContainer](<span class="apiarg">bagID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetItemDetails ItemUtil.GetItemDetails](<span class="apiarg">itemLink, quantity, isCurrency, lootSource</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=PickupBagItem ItemUtil.PickupBagItem](<span class="apiarg">itemLocation</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetOptionalReagentCount ItemUtil.GetOptionalReagentCount](<span class="apiarg">itemID</span>)

====MapUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=IsMapTypeZone MapUtil.IsMapTypeZone](<span class="apiarg">mapID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetMapParentInfo MapUtil.GetMapParentInfo](<span class="apiarg">mapID, mapType, topMost</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ShouldMapTypeShowQuests MapUtil.ShouldMapTypeShowQuests](<span class="apiarg">mapType</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ShouldShowTask MapUtil.ShouldShowTask](<span class="apiarg">mapID, info</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=MapHasUnlockedBounties MapUtil.MapHasUnlockedBounties](<span class="apiarg">mapID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=MapHasEmissaries MapUtil.MapHasEmissaries](<span class="apiarg">mapID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=FindBestAreaNameAtMouse MapUtil.FindBestAreaNameAtMouse](<span class="apiarg">mapID, normalizedCursorX, normalizedCursorY</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetDisplayableMapForPlayer MapUtil.GetDisplayableMapForPlayer]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetBountySetMaps MapUtil.GetBountySetMaps](<span class="apiarg">bountySetID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetMapCenterOnMap MapUtil.GetMapCenterOnMap](<span class="apiarg">mapID, topMapID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsChildMap MapUtil.IsChildMap](<span class="apiarg">mapID, ancestorMapID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsOribosMap MapUtil.IsOribosMap](<span class="apiarg">mapID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsShadowlandsZoneMap MapUtil.IsShadowlandsZoneMap](<span class="apiarg">mapID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=MapShouldShowWorldQuestFilters MapUtil.MapShouldShowWorldQuestFilters](<span class="apiarg">mapID</span>)

====PVPUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetTierName PVPUtil.GetTierName](<span class="apiarg">tierEnum</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ShouldShowLegacyRewards PVPUtil.ShouldShowLegacyRewards]()

====PartyUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetMinLevel PartyUtil.GetMinLevel]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetPhasedReasonString PartyUtil.GetPhasedReasonString](<span class="apiarg">phaseReason, unitToken</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetGroupMemberCountsForDisplay GetGroupMemberCountsForDisplay]()

====PlayerUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetCurrentSpecID PlayerUtil.GetCurrentSpecID]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetSpecName PlayerUtil.GetSpecName]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetSpecNameBySpecID PlayerUtil.GetSpecNameBySpecID]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetSpecIconBySpecID PlayerUtil.GetSpecIconBySpecID]()
: [https://github.com/Gethe/wow-ui-source/search?q=ShouldUseNativeFormInModelScene PlayerUtil.ShouldUseNativeFormInModelScene]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetClassID PlayerUtil.GetClassID]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetClassName PlayerUtil.GetClassName]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetClassInfo PlayerUtil.GetClassInfo]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetClassFile PlayerUtil.GetClassFile]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetClassColor PlayerUtil.GetClassColor]()
: [https://github.com/Gethe/wow-ui-source/search?q=CanUseClassTalents PlayerUtil.CanUseClassTalents]()
: [https://github.com/Gethe/wow-ui-source/search?q=HasFriendlyReaction PlayerUtil.HasFriendlyReaction]()

====QuestUtils====
: [https://github.com/Gethe/wow-ui-source/search?q=GetWorldQuestAtlasInfo QuestUtil.GetWorldQuestAtlasInfo](<span class="apiarg">worldQuestType, inProgress, tradeskillLineID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetQuestIconOffer QuestUtil.GetQuestIconOffer](<span class="apiarg">isLegendary, frequency, isRepeatable, isCampaign, isCovenantCalling</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyQuestIconOfferToTexture QuestUtil.ApplyQuestIconOfferToTexture](<span class="apiarg">texture, ...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetQuestIconActive QuestUtil.GetQuestIconActive](<span class="apiarg">isComplete, isLegendary, frequency, isRepeatable, isCampaign, isCovenantCalling</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyQuestIconActiveToTexture QuestUtil.ApplyQuestIconActiveToTexture](<span class="apiarg">texture, ...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ShouldQuestIconsUseCampaignAppearance QuestUtil.ShouldQuestIconsUseCampaignAppearance](<span class="apiarg">questID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetQuestIconOfferForQuestID QuestUtil.GetQuestIconOfferForQuestID](<span class="apiarg">questID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyQuestIconOfferToTextureForQuestID QuestUtil.ApplyQuestIconOfferToTextureForQuestID](<span class="apiarg">texture, ...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetQuestIconActiveForQuestID QuestUtil.GetQuestIconActiveForQuestID](<span class="apiarg">questID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=ApplyQuestIconActiveToTextureForQuestID QuestUtil.ApplyQuestIconActiveToTextureForQuestID](<span class="apiarg">texture, ...</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=SetupWorldQuestButton QuestUtil.SetupWorldQuestButton](<span class="apiarg">button, info, inProgress, selected, isCriteria, isSpellTarget, isEffectivelyTracked</span>)

====RuneforgeUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetCostsString RuneforgeUtil.GetCostsString](<span class="apiarg">costs</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=IsUpgradeableRuneforgeLegendary RuneforgeUtil.IsUpgradeableRuneforgeLegendary](<span class="apiarg">itemLocation</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetRuneforgeFilterText RuneforgeUtil.GetRuneforgeFilterText](<span class="apiarg">filter</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetPreviewClassAndSpec RuneforgeUtil.GetPreviewClassAndSpec]()

====TitleUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetNameFromTitleMaskID TitleUtil.GetNameFromTitleMaskID](<span class="apiarg">titleMaskID</span>)

====TransmogUtil====
: [https://github.com/Gethe/wow-ui-source/search?q=GetInfoForEquippedSlot TransmogUtil.GetInfoForEquippedSlot](<span class="apiarg">transmogLocation</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CanEnchantSource TransmogUtil.CanEnchantSource](<span class="apiarg">sourceID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetWeaponInfoForEnchant TransmogUtil.GetWeaponInfoForEnchant](<span class="apiarg">transmogLocation</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetBestWeaponInfoForIllusionDressup TransmogUtil.GetBestWeaponInfoForIllusionDressup]()
: [https://github.com/Gethe/wow-ui-source/search?q=GetSlotID TransmogUtil.GetSlotID](<span class="apiarg">slotName</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetSlotName TransmogUtil.GetSlotName](<span class="apiarg">slotID</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=CreateTransmogLocation TransmogUtil.CreateTransmogLocation](<span class="apiarg">slotDescriptor, transmogType, modification</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetTransmogLocation TransmogUtil.GetTransmogLocation](<span class="apiarg">slotDescriptor, transmogType, modification</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetTransmogLocationLookupKey TransmogUtil.GetTransmogLocationLookupKey](<span class="apiarg">slotID, transmogType, modification</span>)
: [https://github.com/Gethe/wow-ui-source/search?q=GetSetIcon TransmogUtil.GetSetIcon](<span class="apiarg">setID</span>)
```