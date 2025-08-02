# API C ChatInfo.SendAddonMessage

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ChatInfo|system=ChatInfo}}
{{api ambox|border=red|image=Inv_gizmo_supersappercharge.png|Please use [[ChatThrottleLib]] or [https://www.wowace.com/projects/ace3/pages/api/ace-comm-3-0 AceComm] – otherwise you will blow up the server.}}
<!--desc-->Sends a message over an addon comm channel.
 result = C_ChatInfo.SendAddonMessage(prefix, message [, chatType [, target]])
        = C_ChatInfo.SendAddonMessageLogged

==Arguments==
:;prefix:{{apitype|string}} - Message prefix, can be used as your addon identifier; at most 16 characters.
:;message:{{apitype|string}} - Text to send, at most 255 characters. All characters (decimal ID 1-255) are permissible except NULL (ASCII 0).
:;chatType:{{apitype|string?|default="PARTY"}} - The addon channel to send to.
:;target:{{apitype|string,number?}} - The player name or custom channel number receiving the message for <code>"WHISPER"</code> or <code>"CHANNEL"</code> chatTypes.

==Returns==
:;result:{{apitype|Enum.SendAddonMessageResult}} - Result code indicating if the message has been enqueued by the API for submission. This does not mean that the message has yet been sent, and may still be subject to any server-side throttling.
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|Success}} || 
|-
| 1 || {{apiname|InvalidPrefix}} || 
|-
| 2 || {{apiname|InvalidMessage}} || 
|-
| 3 || {{apiname|AddonMessageThrottle}} || 
|-
| 4 || {{apiname|InvalidChatType}} || 
|-
| 5 || {{apiname|NotInGroup}} || 
|-
| 6 || {{apiname|TargetRequired}} || 
|-
| 7 || {{apiname|InvalidChannel}} || 
|-
| 8 || {{apiname|ChannelThrottle}} || 
|-
| 9 || {{apiname|GeneralError}} || 
|}

==Chat types==
<onlyinclude>{| class="sortable darktable zebra"
! chatType !! Retail !! Classic !! Description
|-
| "PARTY" || <center>✔️</center> || <center>✔️</center> || Addon message to party members.
|-
| "RAID" || <center>✔️</center> || <center>✔️</center> || Addon message to raid members.  If not in a raid group, the message will instead be sent on the PARTY chat type.
|-
| "INSTANCE_CHAT" || <center>✔️</center> || <center>✔️</center> || Addon message to grouped players in instanced content such as dungeons, raids and battlegrounds.
|-
| "GUILD" || <center>✔️</center> || <center>✔️</center> || Addon message to guild members. Prints a ''"You are not in a guild."'' system message if you're not in a guild.
|-
| "OFFICER" || <center>✔️</center> || <center>✔️</center> || Addon message to guild officers.
|-
| "WHISPER" || <center>✔️</center> || <center>✔️</center> || Addon message to a player. Only works for players on the same or any [[Connected Realms|connected]] realms. Use player name as target argument. Prints a ''"Player is offline."'' system message if the target is offline.
|-
| "CHANNEL" || <center>✔️</center> || <center>❌</center> || Addon message to a custom chat channel. Use channel number as target argument. <br>Disabled on Classic to prevent players communicating over custom chat channels.
|-
| "SAY"<ref name="1.13.3">{{ref web|url=https://us.forums.blizzard.com/en/wow/t/wow-classic-patch-1133-lua-api-change/384543|author={{Blizz}}[[Kaivax]]|date=2019-12-09|title=&#91;WoW Classic&#93; Patch 1.13.3 Lua API Change}}</ref> || <center>❌</center> || <center>✔️</center> || Addon message to players within /say range. Subject to heavy throttling and certain specific characters are disallowed.<ref name="valid SAY/YELL characters">{{ref web|url=https://github.com/Stanzilla/WoWUIBugs/issues/23|author=LenweSaralonde|date=2019-12-20|title=String with special characters truncated when sent with C_ChatInfo.SendAddonMessage() over SAY and YELL}}</ref>
|-
| "YELL"<ref name="1.13.3" /> || <center>❌</center> || <center>✔️</center> || Addon message to players within /yell range. Subject to heavy throttling and certain specific characters are disallowed.<ref name="valid SAY/YELL characters" />
|}</onlyinclude>

==Details==
* Recipients must register a prefix using {{api|C_ChatInfo.RegisterAddonMessagePrefix}}() to receive its messages via {{api|t=e|CHAT_MSG_ADDON}}. This prefix can be max '''16 characters''' long and it's recommended to use the addon name if possible so other authors can easily see which addon a registered prefix belongs to.
* Prior to [[Patch 11.0.0]], Blizzard has provided a deprecation wrapper for this API that shifts the result code to the second return position. A forward-compatible way to reliably access the enum return value is to use a negative {{api|t=a|select}} index to grab the last return value.

===C_ChatInfo.SendAddonMessageLogged===

Addons transmitting user-generated content should use this API so recipients can report violations of the [https://us.battle.net/support/en/article/42673 Code of Conduct].

* Fires {{api|t=e|CHAT_MSG_ADDON_LOGGED}} when receiving messages sent via this function.
* ''The message has to be plain text for the game masters to read it.'' Moreover, the messages will silently fail to be sent if it contains an unsupported non-printable character. Some amount of metadata is tolerated, but should be kept as minimal as possible to keep the messages readable for Blizzard's game masters. <ref>{{ref web|url=http://infobot.rikers.org/%23wowuidev/20180614.html.gz|author={{Blizz}}TheDanW|date=2018-06-14|title=#wowuidev IRC chat}}</ref>
* This function has been introduced as a solution to growing issues of harassment and doxxing via addon communications, where players would use addons to send content against the terms of service to other players (roleplaying addons are particularly affected as they offer a free form canvas to share a RP profiles). As regular addon messages are not logged they cannot be seen by game master, they had no way to act upon this content. If you use this function, game masters will be able to check the addon communication logs in case of a report and act upon the content. Users should report addon content that is against the terms of service using Blizzard's support website via the [https://battle.net/support/help/product/wow/197/1501/channels Harassment in addon text] option.

==Message throttling==

Communications on all chat types are subject to a per-prefix throttle. Additionally, if too much data is being sent simultaneously on separate prefixes then the client '''may be disconnected'''. For this reason it is strongly recommended to use [[ChatThrottleLib]] or [https://www.wowace.com/projects/ace3/pages/api/ace-comm-3-0 AceComm] to manage the queueing of messages.

* Each registered prefix is given an allowance of 10 addon messages that can be sent.
* Each message sent on a prefix reduces this allowance by 1.
* If the allowance reaches zero, further attempts to send messages on the same prefix will fail, returning <code>Enum.SendAddonMessageResult.AddonMessageThrottle</code> to the caller.
* Each prefix regains its allowance at a rate of 1 message per second, up to the original maximum of 10 messages.
* This restriction does not apply to whispers outside of instanced content.
* All numbers provided above are the default values, however these can be dynamically reconfigured by the server at any time.

==Example==
Whispers yourself an addon message when you login or /reload
<syntaxhighlight lang="lua">
local prefix = "SomePrefix123"
local playerName = UnitName("player")

local function OnEvent(self, event, ...)
	if event == "CHAT_MSG_ADDON" then
		print(event, ...)
	elseif event == "PLAYER_ENTERING_WORLD" then
		local isLogin, isReload = ...
		if isLogin or isReload then
			C_ChatInfo.SendAddonMessage(prefix, "You can't see this message", "WHISPER", playerName)
			C_ChatInfo.RegisterAddonMessagePrefix(prefix)
			C_ChatInfo.SendAddonMessage(prefix, "Hello world!", "WHISPER", playerName)
		end
	end
end

local f = CreateFrame("Frame")
f:RegisterEvent("CHAT_MSG_ADDON")
f:RegisterEvent("PLAYER_ENTERING_WORLD")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight>

==Libraries==
There is a server-side throttle on in-game addon communication so it's recommended to serialize, compress and encode data before you send them over the addon comms channel.

'''Serialize:'''
* {{api|t=a|C_EncodingUtil.SerializeCBOR}} and {{api|t=a|C_EncodingUtil.DeserializeCBOR}}
* {{api|t=a|C_EncodingUtil.SerializeJSON}} and {{api|t=a|C_EncodingUtil.DeserializeJSON}}
* [https://github.com/rossnichols/LibSerialize LibSerialize] ([https://www.townlong-yak.com/globe/wut/#q:LibSerialize stats])
* [https://www.wowace.com/projects/ace3/pages/api/ace-serializer-3-0 AceSerializer]

'''Compress/Encode:'''
* {{api|t=a|C_EncodingUtil.CompressString}} and {{api|t=a|C_EncodingUtil.DecompressString}}
* [https://github.com/SafeteeWoW/LibDeflate LibDeflate] ([https://www.townlong-yak.com/globe/wut/#q:LibDeflate stats])
* [https://www.wowace.com/projects/libcompress LibCompress] ([https://www.townlong-yak.com/globe/wut/#q:LibCompress stats])

'''Comms:'''
* [https://www.wowace.com/projects/chatthrottlelib ChatThrottleLib] ([[ChatThrottleLib|docs]], [https://www.townlong-yak.com/globe/wut/#q:ChatThrottleLib stats])
* [https://www.wowace.com/projects/ace3/pages/api/ace-comm-3-0 AceComm]

The LibSerialize project page has detailed examples<ref>{{ref web|author=Ross Nichols|url=https://github.com/rossnichols/LibSerialize#libserialize|title=LibSerialize}}</ref> and documentation for using LibSerialize + LibDeflate and AceComm:
<syntaxhighlight lang="lua">
-- Dependencies: AceAddon-3.0, AceComm-3.0, LibSerialize, LibDeflate
MyAddon = LibStub("AceAddon-3.0"):NewAddon("MyAddon", "AceComm-3.0")
local LibSerialize = LibStub("LibSerialize")
local LibDeflate = LibStub("LibDeflate")

function MyAddon:OnEnable()
    self:RegisterComm("MyPrefix")
end

-- With compression (recommended):
function MyAddon:Transmit(data)
    local serialized = LibSerialize:Serialize(data)
    local compressed = LibDeflate:CompressDeflate(serialized)
    local encoded = LibDeflate:EncodeForWoWAddonChannel(compressed)
    self:SendCommMessage("MyPrefix", encoded, "WHISPER", UnitName("player"))
end

function MyAddon:OnCommReceived(prefix, payload, distribution, sender)
    local decoded = LibDeflate:DecodeForWoWAddonChannel(payload)
    if not decoded then return end
    local decompressed = LibDeflate:DecompressDeflate(decoded)
    if not decompressed then return end
    local success, data = LibSerialize:Deserialize(decompressed)
    if not success then return end

    -- Handle `data`
end
</syntaxhighlight>

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 10.2.7|note=All chat types are now subject to a per-prefix throttle. Now returns a result code, rather than a boolean.}}
* {{Patch 10.2.0|note=The "PARTY" chat type now has a per-prefix throttle.}}
* {{Patch 10.0.2|note=The "RAID" chat type now has a per-prefix throttle as of a hotfix build around Jan 12 2023.}}
* {{Patch 8.0.1|note=Moved to <code>C_ChatInfo.SendAddonMessage()</code> and added <code>C_ChatInfo.SendAddonMessageLogged()</code>}}
* {{Patch 6.0.2|note=Added "CHANNEL" chat type.}}
* {{Patch 4.1.0|note=Added "OFFICER" chat type. Addons should now register which prefixes they want to receive addon messages for using {{api|C_ChatInfo.RegisterAddonMessagePrefix}}()<ref name="4.1.0">{{ref web|url=https://blue.mmo-champion.com/topic/163377-patch-41-addon-messages-will-be-filtered/|author={{Blizz}}[[Zarhym]]|date=2011-03-12|title=Patch 4.1: Addon Messages Will Be Filtered}}</ref>}}
* {{Patch 2.1.0|note=Added "WHISPER" chat type was, as servers will begin to rate throttle regular whispers to alleviate [[spam]] problems.}}
* {{Patch 1.12.0|note=Added as <code>SendAddonMessage()</code><ref name="1.12.0">{{ref web|author={{Blizz}}[[slouken]]|url=http://forums.worldofwarcraft.com/thread.aspx?fn=wow-interface-customization&t=412845&p=#post413354|archiveurl=http://blue.cardplace.com/cache/wow-interface-customization/412845.htm|date=20060712|title=Re: Upcoming 1.12 changes - Concise List}}</ref>}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 4.4.0|note=All chat types are now subject to a per-prefix throttle. Now returns a result code, rather than a boolean.}}
* {{Patch 1.13.4|note=Addon comms are now more severely rate throttled (Applied in a hotfix during build 32466 on May 24 2020) <ref>{{ref web|url=https://github.com/AeroScripts/QuestieDev/issues/1974|author=Questie|date=2020-05-25|title=QuestieSerializer.lua (LUA) errors #1974}}</ref>}}
* {{Patch 1.13.3|note="SAY" and "YELL" are now supported chat types, coincident with removing "CHANNEL" to prevent looking-for-group style addons from proliferating in Classic.<ref name="1.13.3" />}}

==See also==
* {{api|C_ChatInfo.GetRegisteredAddonMessagePrefixes}}()
* {{api|C_ChatInfo.IsAddonMessagePrefixRegistered}}()
* {{api|BNSendGameData}}() - Battle.net equivalent.

==References==
```