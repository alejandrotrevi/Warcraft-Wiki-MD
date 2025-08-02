# API GetAvailableLocales

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the available locale strings.
 locale1, ... = GetAvailableLocales([ignoreLocalRestrictions])

==Arguments==
:;ignoreLocalRestrictions:{{apitype|boolean?}} - If true, returns the complete list of locales.

==Returns==
:;locale1, ...:{{apitype|string}}

==Example==
<syntaxhighlight lang="lua">
/dump GetAvailableLocales() -- "enUS", "esMX", "ptBR" (on a US server)
/dump GetAvailableLocales(true) -- "enUS", "koKR", "frFR", "deDE", "zhCN", "esES", "zhTW", "esMX", "ruRU", "ptBR", "itIT"
</syntaxhighlight>

{{apinavbox|Locales}}
```