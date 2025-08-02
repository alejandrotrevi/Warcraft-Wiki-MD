# API GuildRosterSetPublicNote

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Sets the public note of a guild member.
 GuildRosterSetPublicNote(index, note)

==Arguments==
:;index:{{apitype|number}} - The position a member is in the guild roster. Between 1 and {{api|GetNumGuildMembers}}, or 0 for no selection.
:;note:{{apitype|string}} - Text to be set to the public note of the index.

==Example==
Selecting the member withn the {{api|GetGuildRosterSelection}} function.
 GuildRosterSetPublicNote(GetGuildRosterSelection(), "My Public Note")
```