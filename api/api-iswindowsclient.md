# API IsWindowsClient

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if on a Windows client.
 IsWindowsClient()

----
;''Returns''
:;true - If running on a Windows
:;false - If running on a Mac or Linux Box

----
;''Description''

: Will check the user client and return true if the client is running on a Windows system.
: If running on Linux with WINE, this returns true. IsLinuxClient(); is a relic from the World of Warcraft beta when there was a Linux client available.
```