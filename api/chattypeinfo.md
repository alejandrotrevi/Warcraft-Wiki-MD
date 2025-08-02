# ChatTypeInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
=ChatTypeInfo=
Returns a table with attributes for the different types of messages that appear in the chat frame:

*ChatTypeInfo["SYSTEM"]
*ChatTypeInfo["SAY"]
*ChatTypeInfo["PARTY"]
*ChatTypeInfo["RAID"]
*ChatTypeInfo["GUILD"]
*ChatTypeInfo["OFFICER"]
*ChatTypeInfo["YELL"]
*ChatTypeInfo["WHISPER"]
*ChatTypeInfo["WHISPER_INFORM"]
*ChatTypeInfo["REPLY"]
*ChatTypeInfo["EMOTE"]
*ChatTypeInfo["TEXT_EMOTE"]
*ChatTypeInfo["MONSTER_SAY"]
*ChatTypeInfo["MONSTER_PARTY"]
*ChatTypeInfo["MONSTER_YELL"]
*ChatTypeInfo["MONSTER_WHISPER"]
*ChatTypeInfo["MONSTER_EMOTE"]
*ChatTypeInfo["CHANNEL"]
*ChatTypeInfo["CHANNEL_JOIN"]
*ChatTypeInfo["CHANNEL_LEAVE"]
*ChatTypeInfo["CHANNEL_LIST"]
*ChatTypeInfo["CHANNEL_NOTICE"]
*ChatTypeInfo["CHANNEL_NOTICE_USER"]
*ChatTypeInfo["AFK"]
*ChatTypeInfo["DND"]
*ChatTypeInfo["IGNORED"]
*ChatTypeInfo["SKILL"]
*ChatTypeInfo["LOOT"]
*ChatTypeInfo["MONEY"]
*ChatTypeInfo["OPENING"]
*ChatTypeInfo["TRADESKILLS"]
*ChatTypeInfo["PET_INFO"]
*ChatTypeInfo["COMBAT_MISC_INFO"]
*ChatTypeInfo["COMBAT_XP_GAIN"]
*ChatTypeInfo["COMBAT_HONOR_GAIN"]
*ChatTypeInfo["COMBAT_FACTION_CHANGE"]
*ChatTypeInfo["BG_SYSTEM_NEUTRAL"]
*ChatTypeInfo["BG_SYSTEM_ALLIANCE"]
*ChatTypeInfo["BG_SYSTEM_HORDE"]
*ChatTypeInfo["RAID_LEADER"]
*ChatTypeInfo["RAID_WARNING"]
*ChatTypeInfo["RAID_BOSS_WHISPER"]
*ChatTypeInfo["RAID_BOSS_EMOTE"]
*ChatTypeInfo["FILTERED"]
*ChatTypeInfo["BATTLEGROUND"]
*ChatTypeInfo["BATTLEGROUND_LEADER"]
*ChatTypeInfo["RESTRICTED"]
*ChatTypeInfo["CHANNEL1"]
*ChatTypeInfo["CHANNEL2"]
*ChatTypeInfo["CHANNEL3"]
*ChatTypeInfo["CHANNEL4"]
*ChatTypeInfo["CHANNEL5"]
*ChatTypeInfo["CHANNEL6"]
*ChatTypeInfo["CHANNEL7"]
*ChatTypeInfo["CHANNEL8"]
*ChatTypeInfo["CHANNEL9"]
*ChatTypeInfo["CHANNEL10"]
*ChatTypeInfo["ACHIEVEMENT"]
*ChatTypeInfo["GUILD_ACHIEVEMENT"]

SYSTEM is the yellow messages shown by the system, such as the ones shown at login and server reboot warnings.
CHANNEL is /1 through /10, also known as the zone, trade, and custom channels.

Attributes returned from this table are as follows:

*r - red color
*g - green color
*b - blue color
*id - used to associate lines in a chat frame with a specific chat type, for filtering
*sticky - Whether the channel is "sticky". That is, whether you type into that channel again by default after sending a message, or whether it returns to the last sticky channel you typed into the next time you go to send a message. Default sticky channels are listed [[Chat#Advanced Chat Terminology/Details|here]].
```