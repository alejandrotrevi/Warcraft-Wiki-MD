# API SendChatMessage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|note=<font size="5"><code>SAY</code>, <code>YELL</code> and <code>CHANNEL</code> require a hardware event while outdoors.</font>|icon=inv_mushroom_11}} {{deprecatedapi|future=1|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_DeprecatedChatInfo/Deprecated_ChatInfo.lua#L8-L10}}
Sends a chat message.
 SendChatMessage(msg [, chatType [, languageID [, target]]])

==Arguments==
:;msg:{{apitype|string}} - The message to be sent. Large messages are truncated to max 255 characters, and only [[valid chat message characters]] are permitted.
:;chatType:{{apitype|string?}} - The type of message to be sent, e.g. <code>"PARTY"</code>. If omitted, this defaults to <code>"SAY"</code>
:;languageID:{{apitype|number?}} - The [[languageID]] used for the message. Only works with chatTypes <code>"SAY"</code> and <code>"YELL"</code>, and only if not in a group. If omitted the default language will be used: [[Orcish (language)|Orcish]] for the Horde and [[Common (language)|Common]] for the Alliance, as returned by {{api|GetDefaultLanguage}}()
:;target:{{apitype|number,string?}} - The channel number or player name receiving the message for <code>"WHISPER"</code> or <code>"CHANNEL"</code> chatTypes.

==Chat types==
: HW - denotes if the chatType requires a hardware event when in the outdoor world, i.e. not in an instance/battleground.
{| class="sortable darktable zebra"
! chatType !! Command !! <span title="Requires Hardware Event">HW</span> !! Description
|-
| "SAY" || /s, /say || <center>✔️</center> || Chat message to nearby players
|-
| "EMOTE" || /e, /emote || || Custom text emote to nearby players (See {{api|DoEmote}} for normal emotes)
|-
| "YELL" || /y, /yell || <center>✔️</center> || Chat message to far away players
|-
| "PARTY" || /p, /party || || Chat message to party members
|-
| "RAID" || /ra, /raid || || Chat message to raid members
|-
| "RAID_WARNING" || /rw || || Audible warning message to raid members
|-
| "INSTANCE_CHAT" || /i, /instance || || Chat message to the instance group (Dungeon finder / Battlegrounds / Arena)
|-
| "GUILD" || /g, /guild || || Chat message to guild members
|-
| "OFFICER" || /o, /officer || || Chat message to guild officers
|-
| "WHISPER" || /w, /whisper<br>/t, /tell || || Whisper to a specific other player, use player name as '''target''' argument
|-
| "CHANNEL" || /1, /2, ... || <center>✔️<ref>The "CHANNEL" chatType is HW event restricted for both outdoors and indoors.</ref></center> || Chat message to a specific global/custom chat channel, use channel number as '''target''' argument
|-
| "AFK" || /afk || || Not a real channel; Sets your [[AFK]] message. Send an empty message to clear AFK status.
|-
| "DND" || /dnd || || Not a real channel; Sets your [[DND]] message. Send an empty message to clear DND status.
|-
| "VOICE_TEXT" ||  || || Sends text-to-speech to the in-game voice chat.
|}
{{reflist}}

==Details==
* Fires [[Events#C_ChatInfo|CHAT_MSG_*]] events, e.g. {{api|t=e|CHAT_MSG_SAY}} and {{api|t=e|CHAT_MSG_CHANNEL}}
* "RAID_WARNING" is accessible to raid leaders/assistants, or to all members of a party (when not in a raid)
* "WHISPER" works across all realms in a region, it's not restricted to connected realms and you don't need to have interacted with the recipient before.

==Example==
Sends a message, defaults to "SAY".
<syntaxhighlight lang="lua">SendChatMessage("Hello world")</syntaxhighlight>

Sends a /yell message.
<syntaxhighlight lang="lua">SendChatMessage("For the Horde!", "YELL"); DoEmote("FORTHEHORDE")</syntaxhighlight>

Sends a message to [[General Chat]] which is usually on channel index 1
<syntaxhighlight lang="lua">SendChatMessage("Hello friends", "CHANNEL", nil, 1)</syntaxhighlight>

Whispers your target.
<syntaxhighlight lang="lua">SendChatMessage("My, you're a tall one!", "WHISPER", nil, UnitName("target"))</syntaxhighlight>

Sets your /dnd message.
<syntaxhighlight lang="lua">SendChatMessage("Grabbing a beer", "DND")</syntaxhighlight>

Speaks in [[Thalassian]], provided your character knows the language.
<syntaxhighlight lang="lua">SendChatMessage("Ugh, I hate Thunder Bluff! You can't find a good burger anywhere.", "SAY", 10)</syntaxhighlight>

Sends a message to an instance group, raid, or party.
<syntaxhighlight lang="lua">SendChatMessage("Hello there o/", IsInGroup(LE_PARTY_CATEGORY_INSTANCE) and "INSTANCE_CHAT" or IsInRaid() and "RAID" or "PARTY")</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.0|note=Added "VOICE_TEXT"}}
* {{Patch 8.2.5|note=Including [[Patch 1.13.3/API_changes|Patch 1.13.3]]; Partially protected; "SAY", "YELL" and "CHANNEL" must be triggered by a hardware event <ref name="8.2.5">{{ref web|url=https://twitter.com/deadlybossmods/status/1176685822223011842|author=Deadly Boss Mods|date=2019-09-25 16:45|title=SendChatMessage restrictions|quote=''Ok, a bunch of addon authors got to bottom of it after tons of testing. SendChatMessage automation disabled in public/private chat channels It’s ALSO disabled from SAY/YELL out in world. It’s permitted in raid/party/guild chat, and SAY/YELL within instances.''}}</ref>}}
* {{Patch 5.1.0|note=Added "INSTANCE_CHAT" and removed "BATTLEGROUND"}}
* {{Patch 5.0.4|note=Changed language argument from a string to a numeric [[languageID]]}}
* {{Patch 2.4|note=Large messages are truncated to 255 characters and no longer trigger disconnects}}
* {{Patch 2.0.1|note=Throws an error when attempting to speak a language you don't know}}
* {{Patch 1.11.0|note=Added "RAID_WARNING" for raid leaders (subsequently available in party mode by all party members circa Patch 2.0)}}

==References==
<!-- luals
---@param msg string
---@param chatType? ChatType
---@param languageID? number
---@param target? number|string
function SendChatMessage(msg, chatType, languageID, target) end
-->
```