# API GuildRosterSetOfficerNote

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Sets the officer note of a guild member.
 GuildRosterSetOfficerNote(index, note)

==Arguments==
:;index:{{apitype|number}} - The position a member is in the guild roster. Between 1 and {{api|GetNumGuildMembers}}, or 0 for no selection.
:;note:{{apitype|string}} - Text for the officer note.

==Example==
 GuildRosterSetOfficerNote(GetGuildRosterSelection(), "My Officer Note")

==Details==
Color can be added to public notes, officer notes, guild info and guild MOTD using [[UI Escape Sequences]]
 /run GuildRosterSetOfficerNote(GetGuildRosterSelection(), "\124cFFFF0000This Looks Red!")
```