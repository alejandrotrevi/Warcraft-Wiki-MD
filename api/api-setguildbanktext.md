# API SetGuildBankText

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Modifies info text for a tab.
 SetGuildBankText(tab, infoText)

==Arguments==
:;tab:{{apitype|number}} - Bank Tab to edit.
:;infoText:{{apitype|string}} - Text to set, at most 2047 characters

==Details==
* Although the function accepts up to 2047 characters, the standard interface displays only 500.

==See also==
* {{api|GetGuildBankText}}

==External links==
{{Elinks-api|t=a}}
```