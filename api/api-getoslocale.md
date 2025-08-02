# API GetOSLocale

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the locale of the Operating System.
 locale = GetOSLocale()

==Returns==
:;locale:{{apitype|string}} - Recognized values are:<sup>[https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/SharedXML/VideoOptionsPanels.lua#L1270]</sup>
<syntaxhighlight lang="lua">
LanguageRegions = {}
LanguageRegions["deDE"] = 0;
LanguageRegions["enGB"] = 1;
LanguageRegions["enUS"] = 2;
LanguageRegions["esES"] = 3;
LanguageRegions["frFR"] = 4;
LanguageRegions["koKR"] = 5;
LanguageRegions["zhCN"] = 6;
LanguageRegions["zhTW"] = 7;
LanguageRegions["enCN"] = 8;
LanguageRegions["enTW"] = 9;
LanguageRegions["esMX"] = 10;
LanguageRegions["ruRU"] = 11;
LanguageRegions["ptBR"] = 12;
LanguageRegions["ptPT"] = 13;
LanguageRegions["itIT"] = 14;
</syntaxhighlight>
{{apinavbox|Locales}}
```