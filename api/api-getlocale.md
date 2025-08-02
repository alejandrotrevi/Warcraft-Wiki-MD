# API GetLocale

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the game client locale.
 locale = GetLocale()

==Returns==
:;locale:{{apitype|string}}

==Example==
<syntaxhighlight lang="lua">
if GetLocale() == "frFR" then
	print("bonjour")
else
	print("hello")
end
</syntaxhighlight>

==Values==
{{:API GetAvailableLocaleInfo}}

{{apinavbox|Locales}}
```