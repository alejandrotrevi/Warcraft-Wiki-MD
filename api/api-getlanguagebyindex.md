# API GetLanguageByIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the languages that the character can speak by index.
 language, languageID = GetLanguageByIndex(index)

==Arguments==
:;index:{{apitype|number}} - Ranging from 1 up to {{api|GetNumLanguages}}()

==Returns==
:;language:{{apitype|string}}
:;languageID:{{apitype|number}} : [[LanguageID]]

==Example==
<onlyinclude>Prints the available languages for the player.
<syntaxhighlight lang="lua">
for i = 1, GetNumLanguages() do
	print(GetLanguageByIndex(i))
end

-- e.g. for Blood elf
> "Orcish", 1
> "Thalassian", 10
</syntaxhighlight></onlyinclude>

==Values==
{{:LanguageID}}
```