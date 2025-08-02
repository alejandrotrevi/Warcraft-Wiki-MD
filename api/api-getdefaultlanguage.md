# API GetDefaultLanguage

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the character's default language.
 language, languageID = GetDefaultLanguage()

==Returns==
:;language:{{apitype|string}} - The player's default language, usually the faction's common language (i.e. "Common" and "Orcish").
:;languageID:{{apitype|number}} : [[LanguageID]]

==Example==
 /dump GetDefaultLanguage()

 > "Common", 7
```