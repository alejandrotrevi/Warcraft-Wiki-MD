# User defined functions

**Contributor:** Mordecay

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}

These are cut-and-paste functions that you can use in your addons, submitted by {{SITENAME}} contributors.

==API==
The following functions aim at extending the information WoW API provides; some are provided by specialized addons rather than being copy/pastable.
:[[GetMinimapShape]]() - Returns a string describing the shape of the minimap (square? round? and more)
:[[allAreType]](type,...) - Returns true if all the additional parameters are of the type specified.

==Arguments & Returns==
: [[setArgs]](myTable, "name", ...) - remember list of arguments to use for a callback
: [[getArgs]](myTable, "name", ...) - retreive stored list of arguments, plus optional extras
: [[GetReturnValues]](order, functionCall) - Get the return values from ''functionCall'' in any ''order'' you want.

==Color Functions==
:[[ColorGradient]](perc, R1, G1, B1, R2, G2, B2[, ...]) - Converts a percent value into a gradient from 2 or more RGB values
:[[HexToRGB]]("string") - Converts a hex color string to RGB values (0-255)
:[[HexToRGBPerc]]("string") - Converts a hex color string to RGB values (0.0-1.0)
:[[RGBToHex]](red, green, blue) - Converts a RGB value (0-255) into a hex string
:[[RGBPercToHex]](red, green, blue) - Converts a RGB value (0.0-1.0) into a hex string

==Cursor Functions==
:[[GetCursorScaledPosition]]() - Return the exact position the cursor is at based on scale.

==Event Functions==
:[[User:Egingell/PLAYER MONEY|PLAYER_MONEY]] - Add a message to the chat frame when you gain or spend money.

==Frame Functions==
: [[GetQuadrant]](frame) - Find which quadrant of the screen a frame lies in.
: [[GetUIParentAnchor]](frame) - Returns SetPoint args for the frame, anchor is relative to the nearest corner of the screen.
: [[Frame:RegisterEvents]](...) - Register '''n''' number of events at once.
: [[Frame:UnregisterEvents]](...) - Unregister '''n''' number of events at once.
: [[Frame:SetManyAttributes]](...) - Simple function to embed in a frame to set many atributes at once.
: [[UnregisterEventFromAllFrames]](event) - Tell all the frames listening for '''event''' to stop listening for it.
: [[addDropDownMenuButton]](uid, dropdown, index, title, usable, onClick [, hint]) - Adds a new button to a drop down (right-click popup) list of your choice.

==Guild Functions==
:[[GuildNameToIndex]](name, searchOffline) - Takes a name and converts it to their index within the guild for other guild functions.

==Item Functions==
:[[EquipItemByLink]](link) - Equips the first matching item found in the player's bags.
:[[GetItemInfoDelayed]](itemID or "itemString" or "itemName" or "itemLink") - Process item info, delay when necessary.

==Localization Tables==
: [[LocalizedClassNames]] - Table of localized classes

==Map Functions==
:[[GetPlayerBearing]]() - Returns the player's current facing bearing based on minimap arrow

==Menu Functions==
:[[Context Menu Maker]] - Pseudo-Class. Add/Remove menu items and show the menu when you're ready.

==Metatables==
: [[Memorizing table]] - A special table that calculates values as needed and saves them into itself

==Number Functions==
: [[round]](input, n) - Round '''input''' to '''n''' places.
: [[truncate]](number, n) - Truncate a number to n decimal places.

==Slash Function==
: [[GetSlashFunc]] - Get an existing slash command function for hooking.
: [[RunSlashCmd]] - Passes a slash command to the chatframe
: [[SlashCmdList AddSlashCommand|SlashCmdList_AddSlashCommand]](name, func, ...)

==String Functions==
:[[ChunkSplit]](string [, length [, endChars]]) - Split a string into groups of "length" each ending with "endChars" (identical to the [http://php.net/chunk-split PHP function] of the same name).
:[[CountChars]](haystack, needle) - Return how many times ''needle'' is contained in ''haystack''.
:[[GetWords]]("string") - Split words on space boundary, return table
:[[printMSG]]("string") - Displays a custom message to the default chat frame, for the user to see (time, code and size saver).
:[[strfindt]](tabCaptures, ...) - Wrapper for [[API strfind|strfind]]() that returns captures in a table - can be used in if() clauses!
:[[StringHash]]("string") - Create a fair-quality 32-bit hash of a string
:[[substr]]("string", start [, length]) - Imp [[API strsub|strsub]]. Returns a string starting from ''start'' to ''length'' characters from ''start'' (identical to the [http://php.net/substr PHP function] of the same name).

==Table Functions==
:[[tinsertbeforeval]](tab, valBefore, val) - Insert one value before another (without knowing its index)
:[[tremovebyval]](tab, val) - Remove a value (without knowing its index)
:[[tcount]](tab) - Count table members (works on non-integer-indexed tables)
:[[tcopy]](tabTo, tabFrom) - Recursively copy contents of one table to another
:[[orderedpairs]](tab[, comparisonFunc]) - Iterate over the table in key/value order specified by comparisonFunc

==Time Functions==
:[[GameTime:Get]]() - Get server time including seconds and milliseconds
:[[wait]](delay,function [, param [,param [,...]]]) - Wait a specified amount of time before running a function with the given parameters.
:[[SecondsToDays]]() - Converts seconds to days/hours/minutes/seconds

==See also==
* [[:Category:HOWTOs]]

[[Category:Interface customization]]
[[Category:User defined functions| User defined functions]]
```