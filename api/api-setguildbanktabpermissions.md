# API SetGuildBankTabPermissions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Modifies the permissions for a guild bank tab.
 SetGuildBankTabPermissions(tab, index, enabled)

==Arguments==
:;tab:{{apitype|number}} - Bank Tab to edit.
:;index:{{apitype|number}} - Index of Permission to edit.
:;enabled:{{apitype|boolean}} - true or false to Enable or Disable permission.


==Details==
Use GuildControlSetRank() to set what rank you are editting permissions for. Will not save until GuildControlSaveRank() is called.<br>

Current Known Index Values:<br>
1 = View Tab<br>
2 = Deposit Item
```