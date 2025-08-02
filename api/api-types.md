# API types

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapitype}}
These are the API types from {{framexml_link|AddOns/Blizzard_APIDocumentationGenerated|name=Blizzard_APIDocumentationGenerated}} and are documented here to keep better track of them.

==Basic types==
* <code>bool</code> : {{apitype|boolean}}
* <code>number</code>
* <code>luaIndex</code> :  {{apitype|number}} - used as an index
* <code>string</code>
* <code>cstring</code> : {{apitype|string}} - interchangeable for string
* <code>table</code>
* <code>luaFunction</code> : {{apitype|function}}

==Mixin objects==
* <code>AzeriteEmpoweredItemLocation</code> - [[ItemLocationMixin]]
* <code>AzeriteItemLocation</code> - [[ItemLocationMixin]]
* <code>colorRGB</code> - [[ColorMixin]]
* <code>colorRGBA</code> - [[ColorMixin]]
* <code>EmptiableItemLocation</code> - [[ItemLocationMixin]]
* <code>ItemLocation</code> - [[ItemLocationMixin]]
* <code>ItemTransmogInfo</code> - [[ItemTransmogInfoMixin]]
* <code>PlayerLocation</code> - [[PlayerLocationMixin]]
* <code>ReportInfo</code> - [[ReportInfoMixin]]
* <code>TransmogLocation</code> - [[TransmogLocationMixin]]
* <code>TransmogPendingInfo</code> - [[TransmogPendingInfoMixin]]
* <code>[[API_types/vector2|vector2]]</code> - [[Vector2DMixin]]
* <code>vector3</code> - [[Vector3DMixin]]

==Widgets==
* <code>CScriptObject</code> - [[UIOBJECT_FrameScriptObject|FrameScriptObject]]
* <code>ModelSceneFrame</code> - [[UIOBJECT_ModelScene|ModelScene]]
* <code>ModelSceneFrameActor</code> - [[UIOBJECT_ModelSceneActor|ModelSceneActor]]
* <code>NamePlateFrame</code> - [[API_C_NamePlate.GetNamePlateForUnit|NamePlate]]
* <code>ScriptRegion</code> - [[UIOBJECT_ScriptRegion|ScriptRegion]]
* <code>SimpleAnim</code> - [[UIOBJECT_Animation|Animation]]
* <code>SimpleAnimGroup</code> - [[UIOBJECT_AnimationGroup|AnimationGroup]]
* <code>SimpleControlPoint</code> - [[UIOBJECT_ControlPoint|ControlPoint]]
* <code>SimpleFont</code> - [[UIOBJECT_Font|Font]]
* <code>SimpleFontString</code> - [[UIOBJECT_FontString|FontString]]
* <code>SimpleFrame</code> - [[UIOBJECT_Frame|Frame]]
* <code>SimpleLine</code> - [[UIOBJECT_Line|Line]]
* <code>SimpleMaskTexture</code> - [[UIOBJECT_MaskTexture|MaskTexture]]
* <code>SimplePathAnim</code> - [[UIOBJECT_Path|Path]]
* <code>SimpleTexture</code> - [[UIOBJECT_Texture|Texture]]
* <code>SimpleWindow</code>

==Enum types==
* <code>BlendMode</code> : {{apitype|string}} - <code>DISABLE, BLEND, ALPHAKEY, ADD, MOD</code>
* <code>ConnectionIptype</code> : {{apitype|number}} - <code>1=IPv4, 2=IPv6</code>
* <code>CurveType</code> : {{apitype|string}} - <code>NONE, SMOOTH</code>
* <code>DrawLayer</code> : {{apitype|string}} - <code>BACKGROUND, BORDER, ARTWORK, OVERLAY, HIGHLIGHT</code>
* <code>FilterMode</code> : {{apitype|string}} - <code>LINEAR, TRILINEAR, NEAREST</code>
* <code>FontAlphabet</code> : {{apitype|string}} - <code>roman, korean, simplifiedchinese, traditionalchinese, russian</code>
* <code>FramePoint</code> : {{apitype|string}} - <code>TOPLEFT, TOPRIGHT, BOTTOMLEFT, BOTTOMRIGHT, TOP, BOTTOM, LEFT, RIGHT, CENTER</code>
* <code>FrameStrata</code> : {{apitype|string}} - <code>PARENT, BACKGROUND, LOW, MEDIUM, HIGH, DIALOG, FULLSCREEN, FULLSCREEN_DIALOG, TOOLTIP, BLIZZARD</code>
* <code>InsertMode</code> : {{apitype|string}} - <code>TOP, BOTTOM</code>
* <code>JustifyHorizontal</code> : {{apitype|string}} - <code>LEFT, CENTER, RIGHT</code>
* <code>JustifyVertical</code> : {{apitype|string}} - <code>TOP, MIDDLE, BOTTOM</code>
* <code>LoopType</code> : {{apitype|string}} - <code>NONE, REPEAT, BOUNCE</code>
* <code>mouseButton</code> : {{apitype|string}} - <code>LeftButton, RightButton, MiddleButton, Button4, Button5</code>
* <code>Orientation</code> : {{apitype|string}} - <code>HORIZONTAL, VERTICAL</code>
* <code>SimpleButtonStateToken</code> : {{apitype|string}} - <code>DISABLED, NORMAL, PUSHED</code>
* <code>SmoothingType</code> : {{apitype|string}} - <code>NONE, IN, OUT, IN_OUT, OUT_IN</code>
* <code>StatusBarFillStyle</code> : {{apitype|string}} - <code>STANDARD, STANDARD_NO_RANGE_FILL, CENTER, REVERSE</code>
* <code>[[Apitype_TBFFlags|TBFFlags]]</code> : {{apitype|string}} - <code>"", MONOCHROME, OUTLINE, THICKOUTLINE</code>

==Special types==
* <code>AnimationDataEnum</code> : {{apitype|number}} - {{dbc|AnimationData}}.ID
* <code>ArtifactTiers</code> : {{apitype|number}}
* <code>BigInteger</code> : {{apitype|number}}
* <code>BigUInteger</code> : {{apitype|number}}
* <code>CalendarEventID</code> : {{apitype|number}}
* <code>ClubId</code> : {{apitype|string}}
* <code>ClubInvitationId</code> : {{apitype|string}}
* <code>ClubStreamId</code> : {{apitype|string}}
* <code>FileAsset</code> : {{apitype|string}}
* <code>[[API_types/fileID|fileID]]</code> : {{apitype|number}} - [[FileID]]
* <code>[[API_types/FunctionContainer|FunctionContainer]]</code> : {{apitype|userdata}} - Wrapper for a Lua function to be executed as a callback
* <code>GarrisonFollower</code> : {{apitype|string}} - [[GUID#Follower]]
* <code>HTMLTextType</code> : {{apitype|string}}
* <code>IDOrLink</code> : {{apitype|number,string}} - ID or [[ItemLink]]
* <code>InventorySlots</code> : {{apitype|number}}
* <code>[[API_types/ItemInfo|ItemInfo]]</code> : {{apitype|number,string}} - Item ID, item [[GUID#Item|GUID]], [[ItemLink]] or name
* <code>kstringClubMessage</code> : {{apitype|string}} - [[Kstring]]
* <code>kstringLfgListApplicant</code> : {{apitype|string}} - [[Kstring]]
* <code>kstringLfgListChat</code> : {{apitype|string}} - [[Kstring]]
* <code>kstringLfgListSearch</code> : {{apitype|string}} - [[Kstring]]
* <code>LuaValueVariant</code> : {{apitype|table}}
* <code>ModelAsset</code> : {{apitype|number}} - [[FileID]]
* <code>normalizedValue</code> : {{apitype|number}} - <code>[0.0 - 1.0]</code>
* <code>NotificationDbId</code> : {{apitype|string}}
* <code>RecruitAcceptanceID</code> : {{apitype|string}}
* <code>SingleColorValue</code> : {{apitype|number}}
* <code>size</code> : {{apitype|number}}
* <code>[[API_types/SpellIdentifier|SpellIdentifier]]</code> : {{apitype|number,string}} - Spell ID, name, name(subtext), or [[Hyperlinks#spell|link]]
* <code>stringView</code> : {{apitype|string}}
* <code>TextureAsset</code> : {{apitype|number,string,Texture}} - [[FileID]] or Texture name/object
* <code>TextureAssetDisk</code> : {{apitype|number,string}} - [[FileID]] or path
* <code>textureAtlas</code> : {{apitype|string}} - [[AtlasID]]
* <code>textureKit</code> : {{apitype|string}} - {{dbc|UiTextureKit}}.KitPrefix
* <code>time_t</code> : {{apitype|number}} - Time in seconds
* <code>[[API_types/uiAddon|uiAddon]]</code> : {{apitype|number,string}} - AddOn index or name
* <code>uiFontHeight</code> : {{apitype|number}}
* <code>uiRect</code> : list:{{apitype|number}} - A list of numbers (<code>left, right, top, bottom</code>)
* <code>uiUnit</code> : {{apitype|number}}
* <code>[[API_types/UnitToken|UnitToken]]</code> : {{apitype|string}} - [[UnitId]]
* <code>WeeklyRewardItemDBID</code> : {{apitype|string}}
* <code>[[API_types/WOWGUID|WOWGUID]]</code> : {{apitype|string}} - [[GUID]]
* <code>WOWMONEY</code> : {{apitype|number}} - Amount in copper

<!--The [[World of Warcraft API]] is constructed in lua, with an accompanying XML definition, in which everything is either a basic type, function or table.  Tables are flexible objects that the API uses to define rather distinct WoW-specific "complex" types.

==Basic Types==
 ===Lua===
Lua variables are not formally assigned a type, but rather dynamically become a type when a value is assigned.<ref>{{ref book|author=R. Ierusalimschy, L. H. de Figueiredo, W. Celes|url=https://www.lua.org/manual/5.1/manual.html|date=20060801|isbn=85-903798-3-3|title=Lua 5.1 Reference Manual|chapter=2.2 – Values and Types}}</ref>  World of Warcraft uses seven basic types from Lua.
{| class="darktable zebra"
|-
! Type !! Description !! Implicit casting !! Explicit casting !! Special Functions
|-
| <center>{{apitype|nil}}</center> || absence of any value || || ||
|-
| <center>{{apitype|boolean}}</center> || true or false, historically represented as 1 or nil<sup style="color:yellow">†</sup> || nil → false; any other value → true || <code>x = not not x</code> || 
|-
| <center>{{apitype|number}}</center> || integer or floating-point || "1" → 1; "1.23" → 1.23 || {{api|tonumber(x)}} returns a number or nil || [[Lua functions#Math Functions|Math]], [[Lua functions#Bit Functions|Bitlib]]
|-
| <center>{{apitype|string}}</center> || array of UTF-8 characters || 1.23 → "1.23"; true → "true" || {{api|tostring(x)}} returns "nil", "function: x", etc. || [[Lua functions#String Functions|String]]
|-
| <center>{{apitype|function}}</center> || reference to executable code || || ||
|-
| <center>{{apitype|table}}</center> || reference to an association of key/value pairs || || || [[Lua functions#Table Functions|Table]]
|-
| <center>{{apitype|userdata}}</center> || reference to an object implemented in ''C''<sup style="color:yellow">‡</sup> || || ||
|-
| colspan="5" |
:::<span style="color:yellow">†</span> <span style="font-size:smaller">The original WoW API was written in [https://www.lua.org/manual/4.0/manual.html Lua v4] that had no boolean type; the formal definition being introduced in Lua 5.0</span>
:::<span style="color:yellow">‡</span> <span style="font-size:smaller">The Lua-based WoW API rides over a game engine written in ''C''</span>
|}

===XML===
Although XML has 19 primitive data types,<ref>{{Ref web|url=https://www.w3.org/TR/xmlschema-2/#built-in-primitive-datatypes|title=XML Schema Part 2: Datatypes Second Edition|publisher=World Wide Web Consortium|date=20141028|author=XML Schema Working Group}}</ref> FrameXML only uses five corresponding to Lua types:
{| class="darktable zebra"
|-
! Type !! Description !! Runtime (Lua)
|-
| xs:nil || missing or empty attribute || varies by the default value of each attribute
|-
| xs:boolean || "true" or "false" || usually becomes {{apitype|boolean}}
|-
| xs:int || "1" || usually becomes {{apitype|number}}
|-
| xs:float || "1.23" || usually becomes {{apitype|number}}
|-
| xs:string || "abc" || usually becomes a {{apitype|string}} or a {{api|getglobal|globally accessible}} reference (''ie.'' _G["name"])
|}

==API Types==
{{for|the complete list of complex types|:Category:API types}}
The API encodes several complex information using tables and strings.  Although these objects are merely instances of the basic types, their utility comes from how the information is encoded.  Wowpedia's API documentation treates these as '''complex types''' even though there is no such official term.  These may be further categorized as below:

{| class="darktable zebra"
|-
! Category !! Basic Type !! Description
|-
! Numeric ID
| <center>{{apitype|number}}</center> || Whole number enumerating each kind of something, usually ascending from 1 as each expansion adds to the list. <br />(Differs from the enumeration type which is a table with string/number pairs)
: ''Example:'' [[Northrend Dungeonmaster]] has [[achievementID]] <code>1288</code>
|-
! Encoded String
| <center>{{apitype|string}}</center> || Colon-delimited description of an in-game object, usually beginning with its category and ID.
: ''Example:'' [[Hearthstone]] has [[itemString]] <code>"item:6948::::::::80:105::::::"</code>
|-
! Hyperlink 
| <center>{{apitype|string}}</center> || An object string surrounded by <code>|H</code> and <code>|h</code> [[UI escape sequences]], interpretted by chat windows as a clickable hyperlink.
: ''Example:'' [[Arugal's Folly]] has [[questLink]] in <code>|cff808080|Hquest:99:15|h[Arugal's Folly]|h|r</code>
|-
! Globally Unique Identifier ([[GUID]]) 
| <center>{{apitype|string}}</center> || Hyphen-delimited string for every distinguishable object, possibly containing a numeric ID or encoded string in one of the fields.
: ''Example:'' One single [[Kobold Vermin]] in Elwynn Forest might have [[GUID]] <code>Creature-0-6-0-11-31146-000136DF91</code>
|-
! Constant
| <center>''varies''</center> || Global variable (commonly uppercase and underscores) intended to be written in code for legibility and compatibility. <br />The value is fixed (''constant'') during runtime but could differ between classic/retail or languages.
: ''Translation Example:'' [https://www.townlong-yak.com/framexml/live/GlobalStrings.lua FrameXML/GlobalStrings.lua] defines <code>ABSORB = "Absorb"</code> in enUS or <code>ABSORB = "Поглот"</code> in ruRU
: ''Fixed-Value Example:'' [https://www.townlong-yak.com/framexml/live/Constants.lua FrameXML/Constants.lua] defines <code>LOOT_ROLL_TYPE_NEED = 1</code> and <code>LOOT_ROLL_TYPE_GREED = 2</code>
|-
! Enumeration
| <center>{{apitype|table}}</center> || Keys are strings and values are integers used for quick identification. This approach has increasing usage to replace constants. They can be accessed with e.g. <code>/dump Enum.ClubType</code>
: ''Example:'' {{api|Enum Club.ClubType|t=t}} has four keys "BattleNet", "Character", "Guild" and "Other" with values 0 to 3.
|-
! Struct
| <center>{{apitype|table}}</center> || Return values as a consolidated table with several key/value pairs.  This approach has increasing usage in the modern API.<ref>For example, compare [https://wow.gamepedia.com/index.php?title=API_C_Map.GetMapInfo&oldid=5328377 GetMapInfo()] until Legion with {{api|C_Map.GetMapInfo||uiMapID}} after [[Patch 8.0.1]]</ref>
: ''Example:'' {{api|C_Map.GetMapInfo||uiMapID}} returns a single table decribed by [[Struct Map.UiMapDetails]]
|-
! Mixin
| <center>{{apitype|table}}</center> || FrameXML tables whose members are copied into another table using {{api|CreateFromMixins(mixin)}} and often (not always) incorporated into XML virtual templates.
: ''Example:'' [[SpellMixin]] provides standard methods on any Spell object inheriting from it.
|}

==References==
{{Reflist|2}}
--> 

{{API types}}
[[Category:API types| 0]]
```