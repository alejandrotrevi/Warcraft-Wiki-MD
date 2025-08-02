# API GetAvailableLocaleInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the available locales as a table.
 locales = GetAvailableLocaleInfo([ignoreLocaleRestrictions])

==Arguments==
:;ignoreLocaleRestrictions:{{apitype|boolean?}} - If true, returns the complete list of locales.

==Returns==
:;locales:{{apitype|table[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| localeId || {{apitype|number}} ||
|-
| localeName || {{apitype|string}} ||
|}

==Values==
<onlyinclude>{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! localeId !! localeName !! Description
|-
| 1 || enUS || English (United States)<br>''enGB clients return enUS''
|-
| 2 || koKR || Korean (Korea)
|-
| 3 || frFR || French (France)
|-
| 4 || deDE || German (Germany)
|-
| 5 || zhCN || Chinese (Simplified, PRC)
|-
| 6 || esES || Spanish (Spain)
|-
| 7 || zhTW || Chinese (Traditional, Taiwan)
|-
| 8 || esMX || Spanish (Mexico)
|-
| 9 || ruRU || Russian (Russia)
|-
| 10 || ptBR || Portuguese (Brazil)
|-
| 11 || itIT || Italian (Italy)
|}</onlyinclude>

==Patch changes==
* {{Patch 8.3.0|note=Added (Build 33724, Mar 17 2020).}}

{{apinavbox|Locales}}
```